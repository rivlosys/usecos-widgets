# UseCOS Canadian Financial & Automotive Embed Widgets

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Powered by](https://img.shields.io/badge/Engine-UseCOS.app-00DC82.svg)](https://usecos.app)
[![CRA & OSFI Statutory Formulas](https://img.shields.io/badge/Formulas-CRA%20%26%20OSFI-orange.svg)](https://usecos.app/widgets)

Zero-dependency, responsive, privacy-first embeddable widgets for Canadian financial calculators and vehicle lookups. Built for mortgage brokers, automotive dealerships, real estate portals, accounting blogs, and Canadian personal finance websites.

Live Directory & Widget Generator: **[usecos.app/widgets](https://usecos.app/widgets)**

---

## Available Widgets

### 1. Canadian GST / HST Sales Tax Calculator Widget
Accurate provincial and territorial sales tax calculator supporting all 13 Canadian jurisdictions (GST, PST, HST, QST). Includes forward tax calculation and reverse tax breakdown (extract net amount and taxes from a gross total).

#### HTML / Iframe Embed
```html
<iframe
  src="https://usecos.app/widgets/gst"
  width="100%"
  height="460"
  style="border: 1px solid #e2e8f0; border-radius: 12px; max-width: 440px;"
  title="Canadian GST / HST Calculator Widget"
  loading="lazy"
></iframe>
<p style="font-size: 11px; color: #64748b; margin-top: 6px;">
  Powered by <a href="https://usecos.app/gst" target="_blank" rel="noopener">UseCOS Canadian Tax Engine</a>
</p>
```

#### React / Next.js Component
```jsx
export function GstWidget() {
  return (
    <div style={{ maxWidth: 440, width: '100%' }}>
      <iframe
        src="https://usecos.app/widgets/gst"
        width="100%"
        height="460"
        style={{ border: '1px solid #e2e8f0', borderRadius: 12 }}
        title="Canadian GST / HST Calculator Widget"
        loading="lazy"
      />
      <div style={{ fontSize: 11, color: '#64748b', marginTop: 6 }}>
        Formula verified via <a href="https://usecos.app/gst" target="_blank" rel="noreferrer">UseCOS</a>
      </div>
    </div>
  );
}
```

---

### 2. Canadian Mortgage & OSFI B-20 Stress Test Widget
Real-time Canadian mortgage payment breakdown with the mandatory **OSFI B-20 Qualifying Rate** (+200 bps above contract rate), monthly amortization schedule, CMHC insurance premium tiers, and municipal property tax estimations.

#### HTML / Iframe Embed
```html
<iframe
  src="https://usecos.app/widgets/mortgage"
  width="100%"
  height="540"
  style="border: 1px solid #e2e8f0; border-radius: 12px; max-width: 480px;"
  title="Canadian Mortgage & Stress Test Calculator"
  loading="lazy"
></iframe>
<p style="font-size: 11px; color: #64748b; margin-top: 6px;">
  Calculation engine by <a href="https://usecos.app" target="_blank" rel="noopener">UseCOS Financial Platform</a>
</p>
```

---

### 3. NHTSA Vehicle VIN Decoder & Safety Recall Lookup Widget
Instant 17-character VIN specification decoder and NHTSA safety recall inspection. Formatted for used car dealerships, classifieds, automotive blogs, and cross-border US-Canada vehicle importers.

#### HTML / Iframe Embed
```html
<iframe
  src="https://usecos.app/widgets/vin"
  width="100%"
  height="520"
  style="border: 1px solid #e2e8f0; border-radius: 12px; max-width: 480px;"
  title="NHTSA Vehicle VIN Decoder Widget"
  loading="lazy"
></iframe>
<p style="font-size: 11px; color: #64748b; margin-top: 6px;">
  Decode vehicle specs & recalls at <a href="https://usecos.app/vin" target="_blank" rel="noopener">UseCOS VIN Decoder</a>
</p>
```

#### Pre-populating a Specific VIN via URL
You can dynamically link directly to a pre-decoded report for private vehicle listings:
```html
<a href="https://usecos.app/vin?vin=1HGCR2F83HA000000" target="_blank" rel="noopener">
  View NHTSA Safety & Specification Report for VIN 1HGCR2F83HA000000
</a>
```

---

## Features

- **No Cookies or User Tracking**: Complies with PIPEDA and GDPR. No third-party ad networks or tracking beacons.
- **Client-Side Rendering**: Fast loading with zero layout shift (CLS).
- **Mobile Responsive**: Adapts seamlessly from 320px smartphones to wide desktop sidebars.
- **Statutory Rules**: Built according to Canada Revenue Agency (CRA) schedules and Office of the Superintendent of Financial Institutions (OSFI) B-20 stress-test criteria.

---

## Web Component (Vanilla JS Custom Element)

If you prefer custom HTML tags `<usecos-gst-widget>` over raw `<iframe>`, include the lightweight loader script:

```html
<script src="https://usecos.app/widgets/loader.js" async></script>

<!-- Add anywhere on your page -->
<usecos-widget type="gst" theme="light"></usecos-widget>
<usecos-widget type="mortgage" theme="light"></usecos-widget>
<usecos-widget type="vin" theme="light"></usecos-widget>
```

---

## Custom Styling & Partner Integrations

For custom branding, headless API access, or white-labeled partner calculations:
- Official Website: [usecos.app](https://usecos.app)
- Widget Catalog: [usecos.app/widgets](https://usecos.app/widgets)
- Issues & Bug Reports: [GitHub Issues](https://github.com/rivlosys/usecos-widgets/issues)

## License
MIT License © 2026 Rivlosys / UseCOS Team.
