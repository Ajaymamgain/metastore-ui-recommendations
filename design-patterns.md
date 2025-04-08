# Metastore UI Design Patterns

## Color System

### Primary Colors
- **Brand Green**: #3dd379 (Used for primary actions, success states)
- **Dark Navy**: #1e2a3b (Used for sidebar, headers)
- **Light Gray**: #f5f7fa (Used for backgrounds, cards)
- **White**: #ffffff (Used for content areas, text on dark backgrounds)

### Secondary Colors
- **Alert Red**: #e74c3c (Used for errors, warnings)
- **Info Blue**: #3498db (Used for information messages)
- **Warning Amber**: #f39c12 (Used for caution states)
- **Neutral Gray**: #95a5a6 (Used for disabled states, secondary text)

## Typography

### Recommended Hierarchy
- **Page Titles**: 24px, SemiBold
- **Section Headers**: 20px, SemiBold
- **Card Titles**: 18px, Medium
- **Body Text**: 16px, Regular
- **Secondary Text**: 14px, Regular
- **Small Text/Labels**: 12px, Medium

### Font Family
- Primary: Inter or SF Pro Display (Sans-serif)
- Monospace: SF Mono (for code or technical content)

## Component Design Improvements

### Card Components
Current cards lack visual hierarchy and data visualization. Recommended improvements:

```
┌────────────────────────────┐
│ Total Stores               │
│                    ┌─────┐ │
│ 3                  │ 📊 │ │
│                    └─────┘ │
│ ↗ +1 from last week        │
│                            │
│ View Details >             │
└────────────────────────────┘
```

### Navigation
Current sidebar navigation could be improved with better active states:

```
┌───────────────────┐
│ Metastore         │
│                   │
│ ○ Dashboard       │
│                   │
│ ● Stores          │ ← Active state with left accent bar
│                   │
│ ○ Products        │
│                   │
│ ○ Orders          │
└───────────────────┘
```

### Form Validation
Improve error messaging by placing it directly under the relevant field:

```
┌────────────────────────────┐
│ Email address              │
│ ┌──────────────────────┐   │
│ │ hello@example.com    │   │
│ └──────────────────────┘   │
│                            │
│ Password                   │
│ ┌──────────────────────┐   │
│ │ ••••••••••           │👁️│
│ └──────────────────────┘   │
│ Password must be at least  │
│ 8 characters               │
└────────────────────────────┘
```

## Empty States

Current empty states use generic placeholders. Recommended improvements:

```
┌────────────────────────────┐
│                            │
│          📦                │
│                            │
│    No products yet         │
│                            │
│  Create your first product │
│  to start selling online   │
│                            │
│     [Create Product]       │
│                            │
└────────────────────────────┘
```

## Loading States

Replace generic skeleton loaders with more realistic placeholders:

```
┌────────────────────────────┐
│ ████████████               │
│                            │
│ ███████                    │
│ ███████████████████        │
│                            │
│ ███████████   ███████      │
│                            │
└────────────────────────────┘
```

## Mobile Optimization

Responsive design patterns for smaller screens:

1. Collapsible sidebar that transforms into a bottom navigation bar
2. Stacked cards instead of grid layout
3. Simplified data visualizations optimized for touch
4. Larger touch targets (minimum 44x44px)

## Accessibility Improvements

- Increased color contrast (minimum 4.5:1 for text)
- Focus indicators for keyboard navigation
- Proper heading hierarchy (H1 → H6)
- Text alternatives for all icons and visual elements
- Support for text resizing up to 200%

## Micro-interactions

Add subtle animations to improve user feedback:

- Button hover/press states
- Smooth transitions between pages
- Loading indicators
- Success/error state animations
- Subtle hover effects on interactive elements