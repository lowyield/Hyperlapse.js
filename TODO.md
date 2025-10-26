# Hyperlapse Revamp To-Do List

## Performance & Smooth Playback
- [ ] Profile WebGL rendering to identify hotspots during texture uploads and camera updates.
- [ ] Implement panorama texture caching keyed by panoId to prevent redundant Street View fetches.
- [ ] Batch Street View metadata requests to respect API quotas while reducing latency spikes.
- [ ] Move image stitching and color correction into Web Workers to keep the main thread responsive on long routes.
- [ ] Add adaptive resolution and frame pacing controls that lower texture size or skip frames on constrained devices.
- [ ] Explore incremental route preloading so that playback can start while downstream frames continue buffering.

## UI / UX Modernization
- [ ] Audit focus order, keyboard shortcuts, and ARIA roles to ensure the viewer is fully accessible.
- [ ] Offer light/dark theme toggles with sensible defaults and saved preferences.
- [ ] Provide contextual tooltips or onboarding hints that explain controls without cluttering the interface.
- [ ] Simplify the control panel layout for touch by increasing target sizes and spacing.

## Mobile & Low-Power Readiness
- [ ] Detect device capabilities to auto-tune resolution, field of view, and animation speed.
- [ ] Add a "battery saver" preset that limits frame rate and disables heavy post-processing.
- [ ] Verify the viewer renders correctly in mobile Safari and Chrome, including orientation changes.
- [ ] Implement offline-aware caching of recent routes when service workers are available.

## Capture & Export
- [ ] Add a frame capture utility that saves the current canvas to an image and exposes a download/share action.
- [ ] Provide a batch capture mode that walks the route and exports sequential frames suitable for video assembly.
- [ ] Consider WebCodecs or WebM export for direct video output when supported.

## Additional Opportunities
- [ ] Publish performance benchmarks and guidance in the README to help others tune their deployments.
- [ ] Create integration hooks for external controllers (e.g., MIDI, gamepads) to support creative playback setups.
- [ ] Evaluate analytics instrumentation to understand common usage patterns and bottlenecks.
# Performance To-Do List

- [ ] Profile WebGL rendering to identify hotspots when updating textures during playback.
- [ ] Implement texture caching to avoid refetching Street View tiles for repeated panorama IDs.
- [ ] Batch Street View metadata requests to respect API quotas while reducing latency.
- [ ] Investigate worker-based image stitching to keep the main thread responsive on large routes.
- [ ] Add adaptive resolution controls that lower texture size on low-powered devices.
