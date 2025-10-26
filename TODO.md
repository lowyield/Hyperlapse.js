# Performance To-Do List

- [ ] Profile WebGL rendering to identify hotspots when updating textures during playback.
- [ ] Implement texture caching to avoid refetching Street View tiles for repeated panorama IDs.
- [ ] Batch Street View metadata requests to respect API quotas while reducing latency.
- [ ] Investigate worker-based image stitching to keep the main thread responsive on large routes.
- [ ] Add adaptive resolution controls that lower texture size on low-powered devices.
