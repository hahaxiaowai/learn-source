
    |-- index.js 入口文件
    |-- css 样式文件夹
    |   |-- mapbox-gl.css css样式
    |   |-- svg 静态图标
    |       |-- mapboxgl-ctrl-attrib.svg
    |       |-- mapboxgl-ctrl-compass.svg
    |       |-- mapboxgl-ctrl-fullscreen.svg
    |       |-- mapboxgl-ctrl-geolocate.svg
    |       |-- mapboxgl-ctrl-logo.svg
    |       |-- mapboxgl-ctrl-shrink.svg
    |       |-- mapboxgl-ctrl-zoom-in.svg
    |       |-- mapboxgl-ctrl-zoom-out.svg
    |-- data 数据相关
    |   |-- array_types.js
    |   |-- bounds_attributes.js
    |   |-- bucket.js
    |   |-- debug_viz.js
    |   |-- dem_data.js
    |   |-- dem_tree.js
    |   |-- evaluation_feature.js
    |   |-- extent.js
    |   |-- feature_index.js
    |   |-- feature_position_map.js
    |   |-- index_array_type.js
    |   |-- load_geometry.js
    |   |-- pos_attributes.js
    |   |-- program_configuration.js
    |   |-- segment.js
    |   |-- bucket
    |       |-- circle_attributes.js
    |       |-- circle_bucket.js
    |       |-- dash_attributes.js
    |       |-- fill_attributes.js
    |       |-- fill_bucket.js
    |       |-- fill_extrusion_attributes.js
    |       |-- fill_extrusion_bucket.js
    |       |-- heatmap_bucket.js
    |       |-- line_attributes.js
    |       |-- line_attributes_ext.js
    |       |-- line_bucket.js
    |       |-- pattern_attributes.js
    |       |-- pattern_bucket_features.js
    |       |-- symbol_attributes.js
    |       |-- symbol_bucket.js
    |-- geo 地理相关计算
    |   |-- edge_insets.js
    |   |-- lng_lat.js
    |   |-- lng_lat_bounds.js
    |   |-- mercator_coordinate.js
    |   |-- transform.js
    |   |-- projection
    |       |-- adjustments.js
    |       |-- albers.js
    |       |-- cylindrical_equal_area.js
    |       |-- equal_earth.js
    |       |-- equirectangular.js
    |       |-- far_z.js
    |       |-- flat_tile_transform.js
    |       |-- globe.js
    |       |-- globe_tile_transform.js
    |       |-- index.js
    |       |-- lambert.js
    |       |-- mercator.js
    |       |-- natural_earth.js
    |       |-- resample.js
    |       |-- tile_transform.js
    |       |-- winkel_tripel.js
    |-- gl gl相关
    |   |-- color_mode.js
    |   |-- context.js
    |   |-- cull_face_mode.js
    |   |-- depth_mode.js
    |   |-- framebuffer.js
    |   |-- index_buffer.js
    |   |-- stencil_mode.js
    |   |-- types.js
    |   |-- value.js
    |   |-- vertex_buffer.js
    |-- render 绘制渲染相关
    |   |-- draw_background.js
    |   |-- draw_circle.js
    |   |-- draw_collision_debug.js
    |   |-- draw_custom.js
    |   |-- draw_debug.js
    |   |-- draw_fill.js
    |   |-- draw_fill_extrusion.js
    |   |-- draw_globe_atmosphere.js
    |   |-- draw_heatmap.js
    |   |-- draw_hillshade.js
    |   |-- draw_line.js
    |   |-- draw_raster.js
    |   |-- draw_sky.js
    |   |-- draw_symbol.js
    |   |-- fog.js
    |   |-- glyph_atlas.js
    |   |-- glyph_manager.js
    |   |-- image_atlas.js
    |   |-- image_manager.js
    |   |-- line_atlas.js
    |   |-- painter.js
    |   |-- program.js
    |   |-- raster_fade.js
    |   |-- skybox_attributes.js
    |   |-- skybox_geometry.js
    |   |-- texture.js
    |   |-- uniform_binding.js
    |   |-- vertex_array_object.js
    |   |-- program
    |       |-- background_program.js
    |       |-- circle_program.js
    |       |-- clipping_mask_program.js
    |       |-- collision_program.js
    |       |-- debug_program.js
    |       |-- fill_extrusion_program.js
    |       |-- fill_program.js
    |       |-- heatmap_program.js
    |       |-- hillshade_program.js
    |       |-- line_program.js
    |       |-- pattern.js
    |       |-- program_uniforms.js
    |       |-- raster_program.js
    |       |-- skybox_capture_program.js
    |       |-- skybox_program.js
    |       |-- symbol_program.js
    |-- shaders 着色器代码
    |   |-- background.fragment.glsl
    |   |-- background.vertex.glsl
    |   |-- background_pattern.fragment.glsl
    |   |-- background_pattern.vertex.glsl
    |   |-- circle.fragment.glsl
    |   |-- circle.vertex.glsl
    |   |-- clipping_mask.fragment.glsl
    |   |-- clipping_mask.vertex.glsl
    |   |-- collision_box.fragment.glsl
    |   |-- collision_box.vertex.glsl
    |   |-- collision_circle.fragment.glsl
    |   |-- collision_circle.vertex.glsl
    |   |-- debug.fragment.glsl
    |   |-- debug.vertex.glsl
    |   |-- encode_attribute.js
    |   |-- fill.fragment.glsl
    |   |-- fill.vertex.glsl
    |   |-- fill_extrusion.fragment.glsl
    |   |-- fill_extrusion.vertex.glsl
    |   |-- fill_extrusion_pattern.fragment.glsl
    |   |-- fill_extrusion_pattern.vertex.glsl
    |   |-- fill_outline.fragment.glsl
    |   |-- fill_outline.vertex.glsl
    |   |-- fill_outline_pattern.fragment.glsl
    |   |-- fill_outline_pattern.vertex.glsl
    |   |-- fill_pattern.fragment.glsl
    |   |-- fill_pattern.vertex.glsl
    |   |-- globe_atmosphere.fragment.glsl
    |   |-- globe_atmosphere.vertex.glsl
    |   |-- globe_raster.fragment.glsl
    |   |-- globe_raster.vertex.glsl
    |   |-- heatmap.fragment.glsl
    |   |-- heatmap.vertex.glsl
    |   |-- heatmap_texture.fragment.glsl
    |   |-- heatmap_texture.vertex.glsl
    |   |-- hillshade.fragment.glsl
    |   |-- hillshade.vertex.glsl
    |   |-- hillshade_prepare.fragment.glsl
    |   |-- hillshade_prepare.vertex.glsl
    |   |-- line.fragment.glsl
    |   |-- line.vertex.glsl
    |   |-- line_pattern.fragment.glsl
    |   |-- line_pattern.vertex.glsl
    |   |-- raster.fragment.glsl
    |   |-- raster.vertex.glsl
    |   |-- README.md
    |   |-- shaders.js
    |   |-- skybox.fragment.glsl
    |   |-- skybox.vertex.glsl
    |   |-- skybox_capture.fragment.glsl
    |   |-- skybox_capture.vertex.glsl
    |   |-- skybox_gradient.fragment.glsl
    |   |-- symbol_icon.fragment.glsl
    |   |-- symbol_icon.vertex.glsl
    |   |-- symbol_sdf.fragment.glsl
    |   |-- symbol_sdf.vertex.glsl
    |   |-- symbol_text_and_icon.fragment.glsl
    |   |-- symbol_text_and_icon.vertex.glsl
    |   |-- terrain_depth.fragment.glsl
    |   |-- terrain_depth.vertex.glsl
    |   |-- terrain_raster.fragment.glsl
    |   |-- terrain_raster.vertex.glsl
    |   |-- _prelude.fragment.glsl
    |   |-- _prelude.glsl
    |   |-- _prelude.vertex.glsl
    |   |-- _prelude_fog.fragment.glsl
    |   |-- _prelude_fog.vertex.glsl
    |   |-- _prelude_terrain.vertex.glsl
    |-- source 数据源相关
    |   |-- canvas_source.js
    |   |-- geojson_source.js
    |   |-- geojson_worker_source.js
    |   |-- geojson_wrapper.js
    |   |-- image_source.js
    |   |-- load_tilejson.js
    |   |-- pixels_to_tile_units.js
    |   |-- query_features.js
    |   |-- raster_dem_tile_source.js
    |   |-- raster_dem_tile_worker_source.js
    |   |-- raster_tile_source.js
    |   |-- rtl_text_plugin.js
    |   |-- source.js
    |   |-- source_cache.js
    |   |-- source_state.js
    |   |-- tile.js
    |   |-- tile_bounds.js
    |   |-- tile_cache.js
    |   |-- tile_id.js
    |   |-- tile_mesh.js
    |   |-- vector_tile_source.js
    |   |-- vector_tile_worker_source.js
    |   |-- video_source.js
    |   |-- worker.js
    |   |-- worker_source.js
    |   |-- worker_tile.js
    |-- style 渲染样式
    |   |-- create_style_layer.js
    |   |-- evaluation_parameters.js
    |   |-- fog.js
    |   |-- fog_helpers.js
    |   |-- format_section_override.js
    |   |-- light.js
    |   |-- load_glyph_range.js
    |   |-- load_sprite.js
    |   |-- parse_glyph_pbf.js
    |   |-- pauseable_placement.js
    |   |-- properties.js
    |   |-- query_geometry.js
    |   |-- query_utils.js
    |   |-- style.js
    |   |-- style_glyph.js
    |   |-- style_image.js
    |   |-- style_layer.js
    |   |-- style_layer_index.js
    |   |-- terrain.js
    |   |-- validate_style.js
    |   |-- zoom_history.js
    |   |-- style_layer
    |       |-- background_style_layer.js
    |       |-- background_style_layer_properties.js
    |       |-- circle_style_layer.js
    |       |-- circle_style_layer_properties.js
    |       |-- custom_style_layer.js
    |       |-- fill_extrusion_style_layer.js
    |       |-- fill_extrusion_style_layer_properties.js
    |       |-- fill_style_layer.js
    |       |-- fill_style_layer_properties.js
    |       |-- heatmap_style_layer.js
    |       |-- heatmap_style_layer_properties.js
    |       |-- hillshade_style_layer.js
    |       |-- hillshade_style_layer_properties.js
    |       |-- layer_properties.js.ejs
    |       |-- line_style_layer.js
    |       |-- line_style_layer_properties.js
    |       |-- raster_style_layer.js
    |       |-- raster_style_layer_properties.js
    |       |-- sky_style_layer.js
    |       |-- sky_style_layer_properties.js
    |       |-- symbol_style_layer.js
    |       |-- symbol_style_layer_properties.js
    |       |-- typed_style_layer.js
    |-- style-spec 样式规范，约束
    |   |-- CHANGELOG.md
    |   |-- composite.js
    |   |-- declass.js
    |   |-- deref.js
    |   |-- diff.js
    |   |-- empty.js
    |   |-- format.js
    |   |-- group_by_layout.js
    |   |-- migrate.js
    |   |-- package.json
    |   |-- README.md
    |   |-- read_style.js
    |   |-- rollup.config.js
    |   |-- style-spec.js
    |   |-- types.js
    |   |-- validate_mapbox_api_supported.js
    |   |-- validate_style.js
    |   |-- validate_style.min.js
    |   |-- visit.js
    |   |-- bin
    |   |   |-- gl-style-composite
    |   |   |-- gl-style-format
    |   |   |-- gl-style-migrate
    |   |   |-- gl-style-validate
    |   |-- dist
    |   |   |-- .gitkeep
    |   |-- error
    |   |   |-- parsing_error.js
    |   |   |-- validation_error.js
    |   |-- expression
    |   |   |-- compound_expression.js
    |   |   |-- evaluation_context.js
    |   |   |-- expression.js
    |   |   |-- index.js
    |   |   |-- is_constant.js
    |   |   |-- parsing_context.js
    |   |   |-- parsing_error.js
    |   |   |-- runtime_error.js
    |   |   |-- scope.js
    |   |   |-- stops.js
    |   |   |-- types.js
    |   |   |-- values.js
    |   |   |-- definitions
    |   |   |   |-- assertion.js
    |   |   |   |-- at.js
    |   |   |   |-- case.js
    |   |   |   |-- coalesce.js
    |   |   |   |-- coercion.js
    |   |   |   |-- collator.js
    |   |   |   |-- comparison.js
    |   |   |   |-- format.js
    |   |   |   |-- image.js
    |   |   |   |-- in.js
    |   |   |   |-- index.js
    |   |   |   |-- index_of.js
    |   |   |   |-- interpolate.js
    |   |   |   |-- length.js
    |   |   |   |-- let.js
    |   |   |   |-- literal.js
    |   |   |   |-- match.js
    |   |   |   |-- number_format.js
    |   |   |   |-- slice.js
    |   |   |   |-- step.js
    |   |   |   |-- var.js
    |   |   |   |-- within.js
    |   |   |-- types
    |   |       |-- collator.js
    |   |       |-- formatted.js
    |   |       |-- resolved_image.js
    |   |-- feature_filter
    |   |   |-- convert.js
    |   |   |-- index.js
    |   |   |-- README.md
    |   |-- function
    |   |   |-- convert.js
    |   |   |-- index.js
    |   |-- migrate
    |   |   |-- expressions.js
    |   |   |-- v8.js
    |   |   |-- v9.js
    |   |-- reference
    |   |   |-- latest.js
    |   |   |-- v8.json
    |   |-- util
    |   |   |-- color.js
    |   |   |-- color_spaces.js
    |   |   |-- deep_equal.js
    |   |   |-- extend.js
    |   |   |-- get_type.js
    |   |   |-- interpolate.js
    |   |   |-- properties.js
    |   |   |-- ref_properties.js
    |   |   |-- result.js
    |   |   |-- unbundle_jsonlint.js
    |   |-- validate
    |       |-- latest.js
    |       |-- validate.js
    |       |-- validate_array.js
    |       |-- validate_boolean.js
    |       |-- validate_color.js
    |       |-- validate_constants.js
    |       |-- validate_enum.js
    |       |-- validate_expression.js
    |       |-- validate_filter.js
    |       |-- validate_fog.js
    |       |-- validate_formatted.js
    |       |-- validate_function.js
    |       |-- validate_glyphs_url.js
    |       |-- validate_image.js
    |       |-- validate_layer.js
    |       |-- validate_layout_property.js
    |       |-- validate_light.js
    |       |-- validate_number.js
    |       |-- validate_object.js
    |       |-- validate_paint_property.js
    |       |-- validate_projection.js
    |       |-- validate_property.js
    |       |-- validate_source.js
    |       |-- validate_string.js
    |       |-- validate_terrain.js
    |-- symbol 图标相关
    |   |-- anchor.js
    |   |-- check_max_angle.js
    |   |-- clip_line.js
    |   |-- collision_index.js
    |   |-- cross_tile_symbol_index.js
    |   |-- get_anchors.js
    |   |-- grid_index.js
    |   |-- mergelines.js
    |   |-- one_em.js
    |   |-- opacity_state.js
    |   |-- path_interpolator.js
    |   |-- placement.js
    |   |-- projection.js
    |   |-- quads.js
    |   |-- shaping.js
    |   |-- symbol_layout.js
    |   |-- symbol_size.js
    |   |-- transform_text.js
    |-- terrain 地形相关
    |   |-- draw_terrain_raster.js
    |   |-- elevation.js
    |   |-- globe_attributes.js
    |   |-- globe_raster_program.js
    |   |-- terrain.js
    |   |-- terrain_raster_program.js
    |-- types 定义接口类型
    |   |-- callback.js
    |   |-- cancelable.js
    |   |-- tilejson.js
    |   |-- transferable.js
    |   |-- window.js
    |-- ui 窗口样式
    |   |-- anchor.js
    |   |-- camera.js
    |   |-- default_locale.js
    |   |-- events.js
    |   |-- free_camera.js
    |   |-- handler_inertia.js
    |   |-- handler_manager.js
    |   |-- hash.js
    |   |-- map.js
    |   |-- marker.js
    |   |-- popup.js
    |   |-- control
    |   |   |-- attribution_control.js
    |   |   |-- fullscreen_control.js
    |   |   |-- geolocate_control.js
    |   |   |-- logo_control.js
    |   |   |-- navigation_control.js
    |   |   |-- scale_control.js
    |   |-- handler
    |       |-- box_zoom.js
    |       |-- click_zoom.js
    |       |-- handler_util.js
    |       |-- keyboard.js
    |       |-- map_event.js
    |       |-- mouse.js
    |       |-- scroll_zoom.js
    |       |-- tap_drag_zoom.js
    |       |-- tap_recognizer.js
    |       |-- tap_zoom.js
    |       |-- touch_pan.js
    |       |-- touch_zoom_rotate.js
    |       |-- shim
    |           |-- dblclick_zoom.js
    |           |-- drag_pan.js
    |           |-- drag_rotate.js
    |           |-- touch_zoom_rotate.js
    |-- util 工具
        |-- actor.js
        |-- ajax.js
        |-- browser.js
        |-- classify_rings.js
        |-- color_ramp.js
        |-- config.js
        |-- debug.js
        |-- dictionary_coder.js
        |-- dispatcher.js
        |-- dom.js
        |-- eased_variable.js
        |-- evented.js
        |-- find_pole_of_inaccessibility.js
        |-- global_worker_pool.js
        |-- image.js
        |-- intersection_tests.js
        |-- is_char_in_unicode_block.js
        |-- mapbox.js
        |-- offscreen_canvas_supported.js
        |-- performance.js
        |-- primitives.js
        |-- resolve_tokens.js
        |-- scheduler.js
        |-- script_detection.js
        |-- sku_token.js
        |-- smart_wrap.js
        |-- struct_array.js
        |-- struct_array.js.ejs
        |-- struct_array_layout.js.ejs
        |-- task_queue.js
        |-- throttle.js
        |-- throttled_invoker.js
        |-- tile_request_cache.js
        |-- util.js
        |-- vectortile_to_geojson.js
        |-- verticalize_punctuation.js
        |-- webp_supported.js
        |-- web_worker.js
        |-- web_worker_transfer.js
        |-- window.js
        |-- worker_performance_utils.js
        |-- worker_pool.js
        |-- browser
            |-- web_worker.js
            |-- window.js
