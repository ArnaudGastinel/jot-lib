
SET(GTEX_FILES
	basic_texture.C
	gl_extensions.C
	paper_effect.C
	xtoon_texture.C
	toon_texture_1D.C
	color_id_texture.C
	fader_texture.C
	wireframe.C
	control_frame.C
	control_line.C
	solid_color.C
	smooth_shade.C
	flat_shade.C
	normals_texture.C
	sils_texture.C
	creases_texture.C
	key_line.C
	zxsils_texture.C
	ref_image.C
	buffer_ref_image.C
	aux_ref_image.C
	curvature_texture.C
	curvature_ui.C
	line_drawing.C
	perlin.C
	glsl_shader.C
	halftone_shader.C
	halftone_shader_ex.C
	hatching_tx.C
	painterly.C
	glsl_toon.C
	tone_shader.C
	glsl_halo.C
	glsl_marble.C
	glsl_toon_halo.C
	glsl_paper.C
	glsl_xtoon.C
	glsl_solid.C
	glsl_normal.C
	dots.C
	dots_ex.C
	haftone_tx.C
	glsl_hatching.C
	gl_sphir_tex_coord_gen.C
	glsl_layer_base.C
	halo_ref_image.C
	blur_shader.C
	halo_blur_shader.C
	basecoat_shader.C
	multi_lights_tone.C
	patch_id_texture.C)

ADD_LIBRARY(gtex ${GTEX_FILES})

TARGET_LINK_LIBRARIES(gtex
	disp
	dlhandler
	geom
	glew
	mesh
	mlib
	npr
	std
	glui
	${OPENGL_LIBRARY}
	${GLEW_LIBARY})

IF(REF_IMG_32_BIT)
SET_PROPERTY(
	SOURCE ${GTEX_FILES}
	APPEND
	PROPERTY COMPILE_DEFINITIONS
	REF_IMG_32_BIT)
ENDIF(REF_IMG_32_BIT)

