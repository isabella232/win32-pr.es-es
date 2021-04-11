---
title: Preguntas más frecuentes sobre Direct3D 10
description: Este artículo contiene algunas de las preguntas más frecuentes sobre Direct3D 10 desde el punto de vista de un desarrollador que está migrando una aplicación existente de Direct3D 9 (D3D9) a Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149402"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Preguntas más frecuentes sobre Direct3D 10

Este artículo contiene algunas de las preguntas más frecuentes sobre Direct3D 10 desde el punto de vista de un desarrollador que está migrando una aplicación existente de Direct3D 9 (D3D9) a Direct3D 10 (D3D10).

-   [Búferes de constantes](#constant-buffers)
-   [State](#state)
-   [Formatos](#formats)
-   [Vinculación del sombreador](#shader-linkage)
-   [Llamadas a Draw](#draw-calls)
-   [Recursos](#resources)
-   [Profundidad como textura](#depth-as-texture)
-   [MSAA](#msaa)
-   [Bloqueos](#crashes)
-   [Representación de predicado](#predicated-rendering)
-   [Sombreador de geometría](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Búferes de constantes

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>¿Cuál es la mejor manera de actualizar búferes de constantes?
</dt> <dd>

UpdateSubresource y MAP with discard deben ser aproximadamente la misma velocidad. Elija entre ellos en función de cuál copie la cantidad mínima de memoria. Si ya tiene los datos almacenados en memoria en un bloque contiguo, use UpdateSubresource. Si necesita acumular datos de otros lugares, use Map con discard.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>¿Cuál es la peor manera de organizar los búferes de constantes?
</dt> <dd>

El peor rendimiento se realiza colocando todas las constantes de un sombreador determinado en un búfer de constantes. Aunque esta suele ser la manera más fácil de migrar de D3D9 a D3D10, puede perjudicar el rendimiento. Por ejemplo, considere un escenario que usa el siguiente búfer de constantes:

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

El búfer es de 6560 bytes. Supongamos que hay una aplicación con 1000 objetos que se van a representar, 100 de las cuales son mallas con forma de máscaras y 900 son mallas estáticas. Además, supongamos que esta aplicación está usando la asignación de instantáneas con una fuente de luz. Esto significa que hay dos pasos, uno para el mapa de profundidad representado a partir de la luz y otro para el paso de representación hacia delante. Esto da como resultado 2000 llamadas a Draw. Aunque no es necesario que cada llamada a Draw actualice cada parte del búfer de constantes, todo el búfer de constantes se actualiza y se envía a la tarjeta. Esto da como resultado la actualización de 13 MB de datos cada fotograma (2000 llamadas a Draw en el plazo de 6560 KB).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>¿Cuál es la mejor manera de organizar mis búferes de constantes?
</dt> <dd>

La mejor manera es organizar los búferes de constantes según la frecuencia de actualización. Las constantes que se actualizan en frecuencias similares deben estar en el mismo búfer. Por ejemplo, considere el escenario que se presenta en "¿Cuál es la peor manera de organizar los búferes de constantes?", pero con un diseño mejor constante:

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

Los búferes de constantes se dividen por su frecuencia de actualización, pero solo es la mitad de la solución. La aplicación necesita actualizar los búferes de constantes correctamente para sacar el máximo partido de la división. Se asumirá la misma escena anterior: 900 mallas estáticas, las mallas de nivel 100, un paso de luz y un pase hacia delante. También se supone que se almacenarán algunos búferes de constantes por objeto. Esto significa que cada objeto contendrá un VSPerSkinnedCB o un VSPerStaticCB, en función de si está o no o no o no. Hacemos esto para evitar la duplicación de la cantidad de matrices enviadas a través de la canalización.

Dividimos el marco en tres fases. La primera fase es el principio del marco y no implica ninguna representación, solo actualizaciones constantes.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Inicio del marco**
</dt> <dd>

-   Actualizar VSGlobalPerFrameCB para tiempo de aplicación (4 bytes)
-   Update 100 VSPerSkinnedCB para los objetos de la piel 100 (640000 bytes)
-   Actualizar VSPerStaticCB para los objetos estáticos 900 (57600 bytes)

A continuación se encuentra el paso de asignación de instantáneas. Tenga en cuenta que el único búfer de constantes que se actualiza realmente es VSPerPassCB. El resto de búferes de constantes se actualizaron durante el paso de inicio del marco. Aunque todavía necesitamos enlazar estos búferes de constantes, la cantidad de información que se pasa a la tarjeta de vídeo es mínima, ya que los búferes ya se han actualizado.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Paso de sombra**
</dt> <dd>

-   Actualizar VSPerPassCB (72 bytes)
-   Dibujo de mallas de la piel 100 (100 enlaces, sin actualizaciones)
-   Dibujo de mallas estáticas de 900 (100 enlaces, sin actualizaciones)

Del mismo modo, el paso de representación hacia delante solo necesita actualizar los datos por material, porque no se almacenó por malla. Si damos por hecho que hay 500 materiales en uso en la escena:

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Paso adelante**
</dt> <dd>

-   Actualizar VSPerPassCB (72 bytes)
-   Update 500 VSPerMaterialCBs (10000 bytes)

Esto da como resultado un total de solo 707 KB. Aunque se trata de un escenario muy inventado, muestra la cantidad de sobrecarga de actualización constante que se puede reducir mediante la ordenación de constantes por frecuencia de actualización.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>¿Qué ocurre si no tengo espacio suficiente para almacenar búferes de constantes individuales para mis mallas, material, etc.? 
</dt> <dd>

Siempre puede usar un sistema en capas de búferes de constantes. Cree búferes de constantes de tamaño variable (16 bytes, 32 bytes, 64 bytes, etc.) hasta el tamaño de búfer constante más grande necesario. Cuando sea el momento de enlazar un búfer de constantes a un sombreador, seleccione el búfer de constantes más pequeño que puede contener los datos que necesita el sombreador. Aunque este enfoque es ligeramente menos eficaz, es un buen paso intermedio.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Estoy compartiendo búferes de constantes entre diferentes sombreadores. Un sombreador puede utilizar todas las constantes, pero otra puede utilizar algunas de las constantes. ¿Cuál es la mejor manera de actualizarlos? 
</dt> <dd>

Un enfoque consiste en dividir el búfer de constantes aún más. Sin embargo, llega un momento en el que se enlazan demasiados búferes de constantes. En este caso, mueva las constantes que es probable que estén sin usar en varios sombreadores hasta el final del búfer de constantes. Al obtener los datos de variables del sombreador, use la \_ marca D3D10 SVF \_ Used de la \_ variable de sombreador D3D10 \_ \_ para determinar si se utiliza la variable. Al colocar variables no usadas al final del búfer de constantes, puede enlazar un búfer más pequeño al sombreador que no utiliza estas variables, con lo que se ahorra el costo de actualización.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>¿Cuánto se puede mejorar la velocidad de fotogramas si solo se cargan los huesos de mi carácter una vez por fotograma en lugar de una vez por paso/dibujo? 
</dt> <dd>

Puede mejorar la velocidad de fotogramas entre el 8 y el 50 por ciento, en función de la cantidad de datos redundantes. En el peor de los casos, no se reducirá el rendimiento.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>¿Cuántos búferes de constantes debo haber enlazado a la vez? 
</dt> <dd>

Enlace el número mínimo de búferes de constantes que se tarda en obtener todos los datos en el sombreador. En un escenario realista, cinco es el número recomendado de búferes de constantes que se va a usar. El uso compartido de búferes de constantes entre los sombreadores (enlace de la misma CB a VS y PS) también puede mejorar el rendimiento.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>¿Hay algún costo por enlazar búferes de constantes sin usarlos? 
</dt> <dd>

Sí, si realmente no va a usar el búfer, no llame a VSSetConsantBuffer o PSSetConstantBuffer. Esta sobrecarga adicional de API puede agregarse en el transcurso de varias llamadas a Draw.

</dd> </dl>

## <a name="state"></a>Estado

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>¿Cuál es la mejor manera de administrar el estado en D3D10? 
</dt> <dd>

La mejor solución es conocer todos los Estados por adelantado y crear los objetos de estado por adelantado. Esto significa que, en el momento de la representación, el enlace de estado es la única operación que debe producirse. D3D10 también filtra los duplicados.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mi juego se cargó dinámicamente o tiene contenido generado por el usuario. No puedo cargar todos los objetos de estado por adelantado. ¿Cuál debo hacer? 
</dt> <dd>

Hay dos soluciones aquí. La primera es crear simplemente objetos de estado sobre la marcha y dejar que D3D10 filtre los duplicados. Sin embargo, esto no se recomienda en escenarios con muchos cambios de objetos de estado por fotograma. Una mejor solución consiste en aplicar un algoritmo hash a los objetos de estado y crear un objeto de estado solo si no se encuentra uno que se ajuste a los requisitos en la tabla hash. La razón por la que se usa una tabla hash personalizada es que una aplicación puede seleccionar un hash rápido según el escenario de uso específico de la aplicación. Por ejemplo, si una aplicación solo cambia rendertargetwritemask en BlendState y mantiene todos los demás valores iguales, la aplicación puede generar un hash a partir de rendertargetwritemask en lugar de la estructura completa.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>El estado de AlphaTest ha desaparecido. ¿Dónde estaba? 
</dt> <dd>

AlphaTest Now debe ser rendimiento en el sombreador. Vea el ejemplo FixedFuncEMU.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>¿Qué ha ocurrido con los planos de clips del usuario? 
</dt> <dd>

Los planos de clips del usuario se han pasado al sombreador. Hay dos formas de controlar esto. El primero es la salida \_ de la VP ClipDistance del sombreador de vértices o del sombreador de geometría. La otra opción es usar discard en el sombreador de píxeles en función de algún valor pasado por el sombreador de vértices o el sombreador de geometría. Experimente con ambos para ver cuál es más rápido para su escenario concreto. El uso de VP \_ ClipDistance podría hacer que el hardware utilizara una rutina de recorte basada en geometría que puede provocar que las llamadas de dibujo enlazadas a geometría se ejecuten más lentamente. Del mismo modo, el uso de discard desplaza el trabajo al sombreador de píxeles, lo que puede provocar que las llamadas a Draw enlazadas a píxeles se ejecuten más lentamente.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Los borrados no respetan ninguna configuración de estado, como la configuración de rectángulos de tijeras en mi estado de rasterizador. 
</dt> <dd>

Los borrados se han separado del estado de la canalización. Para obtener el comportamiento del estilo de D3D9, eMule borra el dibujo de un cuádruple de pantalla completa.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Estableció mis Estados de nuevo en predeterminado para probar y diagnosticar un error de representación. Ahora la pantalla aparece en negro, aunque sé que estoy dibujando objetos en la pantalla. 
</dt> <dd>

Al volver a establecer el estado en valores predeterminados (NULL), asegúrese de que SampleMask en la llamada a OMSetBlendState nunca sea cero. Si SampleMask se establece en cero, todos los ejemplos serán lógicamente y con cero. En este escenario, ningún ejemplo pasará la prueba de Blend.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>¿Dónde se D3DSAMP el \_ Estado de SRGBTEXTURE? 
</dt> <dd>

SRGB se quitó como parte del estado de la muestra y ahora está vinculado al formato de textura. Enlazar una textura SRGB dará como resultado el mismo muestreo que obtendría si se especificara D3DSAMP \_ SRGBTEXTURE en Direct3D 9.

</dd> </dl>

## <a name="formats"></a>Formatos

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>¿Qué formato de D3D9 corresponde al formato D3D10? 
</dt> <dd>

Para obtener información, consulte [consideraciones de Direct3D 9 a Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>¿Qué ha ocurrido con los formatos de textura de A8R8G8B8? 
</dt> <dd>

Están en desuso en D3D10. Puede volver a crear las texturas como R8G8B8A8, o puede swizzle en la carga o puede swizzle en el sombreador.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>¿Cómo usar texturas de paleta? 
</dt> <dd>

Coloque la paleta de colores en una textura o en un búfer de constantes y enlácelo a la canalización. En el sombreador de píxeles, realice una búsqueda indirecta mediante el índice en la textura de paleta.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>¿Cuáles son estos nuevos formatos SRGB? 
</dt> <dd>

SRGB se quitó como parte del estado de la muestra y ahora está vinculado al formato de textura. Enlazar una textura SRGB dará como resultado el mismo muestreo que obtendría si se especificara D3DSAMP \_ SRGBTEXTURE en Direct3D 9.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>¿Dónde están los ventiladores de triángulo? 
</dt> <dd>

Los ventiladores de triángulo han quedado en desuso en D3D10. Los ventiladores de triángulo deberán convertirse en la canalización de contenido o en la carga.

</dd> </dl>

## <a name="shader-linkage"></a>Vinculación del sombreador

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Mis sombreadores de Direct3D 9 se compilan correctamente en el modelo de sombreador 4,0, pero cuando se enlazan a la canalización, obtengo errores de vinculación que se muestran en la salida de depuración con el tiempo de ejecución de depuración. 
</dt> <dd>

La vinculación del sombreador es mucho más estricta en D3D10. Los elementos de una fase posterior se deben leer en el orden en que se generan en la fase anterior. Por ejemplo:

Un sombreador de vértices produce:

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Un sombreador de píxeles lee:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Aunque la posición no es necesaria en el sombreador de píxeles, se producirá un error de vinculación, ya que la posición se genera desde el sombreador de vértices, pero no es leída por el sombreador de píxeles. La versión más correcta tendría el siguiente aspecto:

Un sombreador de vértices produce:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Un sombreador de píxeles lee:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

En este caso, el sombreador de vértices está generando la misma información, pero ahora el sombreador de píxeles está leyendo elementos en la salida del pedido. Dado que el sombreador de píxeles no lee nada después de Tex, no es necesario preocuparse de que VS esté generando más información de la que la PS está leyendo.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Necesito una firma de sombreador para crear un diseño de entrada, pero cargaré mis mallas y creo diseños antes de crear los sombreadores. ¿Qué puedo hacer? 
</dt> <dd>

Una solución consiste en cambiar el orden y cargar los sombreadores antes de cargar las mallas. Sin embargo, esto es mucho más fácil decir que listo. Siempre puede crear los diseños de entrada a petición cuando lo necesite la aplicación. Tendrá que mantener una versión de la firma del sombreador en torno a. Debe crear un hash basado en el sombreador y el diseño del búfer, y solo puede crear el diseño de entrada si ya no existe uno que coincida.

</dd> </dl>

## <a name="draw-calls"></a>Llamadas a Draw

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>¿Cuál es el límite de llamadas a Draw para que D3D10 llegue a 60 Hz? ¿30 Hz? 
</dt> <dd>

Direct3D 9 tenía una limitación en cuanto al número de llamadas a Draw debido al costo de CPU por llamada a Draw. En Direct3D 10, se ha reducido el costo de cada llamada a Draw. Sin embargo, ya no existe una correlación definitiva entre las llamadas a Draw y las velocidades de fotogramas. Dado que las llamadas a Draw a menudo requieren muchas llamadas de soporte (actualizaciones de búfer de constantes, enlaces de texturas, configuración de estado, etc.), el impacto de la velocidad de fotogramas de la API ahora es más dependiente del uso general de la API en lugar de simplemente dibujar recuentos de llamadas.

</dd> </dl>

## <a name="resources"></a>Recursos

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>¿Qué tipo de uso de recursos debo usar para las operaciones? 
</dt> <dd>

Use la siguiente hoja de referencia rápida:

-   La CPU actualiza el recurso más de una vez por fotograma: D3D10 \_ Usage \_ Dynamic
-   La CPU actualiza el recurso menos de una vez por fotograma: D3D10 \_ uso \_ predeterminado
-   La CPU no actualiza el recurso: D3D10 \_ Usage \_ inmutable
-   La CPU debe leer el recurso: \_ almacenamiento provisional del uso de D3D10 \_

Dado que los búferes de constantes siempre están diseñados para actualizarse con frecuencia, no se ajustan a la "hoja de referencia". Para saber qué tipos de recursos se deben usar para los búferes de constantes, consulte la sección de [búferes de constantes](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>¿Qué ha ocurrido con DrawPrimitiveUP y DrawIndexedPrimitiveUP? 
</dt> <dd>

Están en D3D10. En el caso de la geometría dinámica, use un búfer dinámico de uso grande de D3D10 \_ \_ . Al principio del marco, asígnelo con D3D10 \_ map \_ Write \_ discard. Para cada llamada subsiguiente a Draw, se avanza el puntero de escritura más allá de la posición de los vértices dibujados previamente y se asigna el búfer con D3D10 \_ map \_ WRITE \_ no \_ overwrite. Si está cerca del final del búfer antes del final del marco, ajuste el puntero de escritura alrededor del principio y asigne el \_ \_ descartado de escritura de asignación de D3D10 \_ .

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>¿Puedo escribir índices de 16 bits y índices de 32 bits en el mismo búfer de geometría dinámico? 
</dt> <dd>

Sí, pero esto puede suponer una reducción del rendimiento en cierto hardware. Es más seguro crear búferes independientes para datos dinámicos de índice de 16 bits y datos de índice de 32 bits.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Cómo leer los datos de la GPU a la CPU? 
</dt> <dd>

Debe utilizar un recurso de almacenamiento provisional. Copie los datos del recurso de GPU en el recurso de almacenamiento provisional mediante CopyResource. Asigne el recurso de almacenamiento provisional para leer los datos.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Mi aplicación depende de la funcionalidad de StretchRect. 
</dt> <dd>

Dado que se trata básicamente de un contenedor para la funcionalidad básica de Direct3D, se quitó de la API. Parte de la funcionalidad de StretchRect se ha pasado a D3DX10LoadTextureFromTexture. En el caso de las conversiones de formato y la copia de texturas, D3DX10LoadTextureFromTexture puede realizar el trabajo. Sin embargo, las operaciones como la conversión de un tamaño a otro probablemente requerirán una operación de representación en la textura en la aplicación.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>No hay desplazamientos ni tamaños en las llamadas de mapa para los recursos. Se trataban de llamadas de bloqueo en Direct3D 9; ¿por qué han cambiado? 
</dt> <dd>

Los desplazamientos y los tamaños de las llamadas de bloqueo en Direct3D 9 eran básicamente el desorden de la API y el controlador los omitió a menudo. Los desplazamientos deben calcularse en su lugar por la aplicación a partir del puntero devuelto en la llamada de asignación.

</dd> </dl>

## <a name="depth-as-texture"></a>Profundidad como textura

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>¿Cuál es más rápido? ¿Usar la profundidad como textura o escribir profundidad en alfa y leer eso? 
</dt> <dd>

Esto es específico de la aplicación y del hardware. Use el que guarde el mayor ancho de banda. Si ya usa varios destinos de representación y tiene un canal adicional, la profundidad de escritura del sombreador puede ser una solución mejor. Además, escribir profundidad en alfa u otro destino de representación permite escribir valores de profundidad lineal que pueden acelerar los cálculos que necesitan tener acceso al búfer de profundidad.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>¿Se puede enlazar una textura como entrada y enlazada como textura de la galería de símbolos de profundidad siempre que se deshabiliten las escrituras de profundidad? 
</dt> <dd>

No está en D3D10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>¿Puedo resolver una textura de la galería de símbolos de profundidad de MSAA? 
</dt> <dd>

No está en D3D10. Sin embargo, puede muestrear ejemplos individuales de la textura de MSAA. Consulte la sección [HLSL](#hlsl) para obtener más información.

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>¿Por qué mi aplicación se bloquea en cuanto habilito MSAA? 
</dt> <dd>

Asegúrese de que está habilitando un recuento de muestras de MSAA y un número de calidad que el controlador enumera realmente.

</dd> </dl>

## <a name="crashes"></a>Bloqueos

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Mi aplicación se bloquea en D3D10 o en el controlador y no sé por qué. 
</dt> <dd>

El primer paso es habilitar el tiempo de ejecución de depuración (D3D10 crear el marcador de [**\_ \_ \_ depuración de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) pasado a [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Esto expondrá los errores más comunes como salida de depuración.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX se bloquea al intentar usar la aplicación con él. 
</dt> <dd>

El primer paso es habilitar el tiempo de ejecución de depuración (D3D10 crear el marcador de [**\_ \_ \_ depuración de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) pasado a [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). PIX tiene una probabilidad mucho mayor de bloqueo si la salida de depuración no está limpia.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mi juego se queda sin espacio de direcciones virtuales en la vista de 32 bits en D3D10. No tiene problemas en D3D9. 
</dt> <dd>

Hubo algunos problemas con D3D10 y el espacio de direcciones virtuales. Esto se ha corregido en [KB940105](https://support.microsoft.com/kb/940105). Si esto no soluciona el problema, asegúrese de que no está creando más recursos que se pueden asignar (bloqueado) en D3D10 de los que estaba creando en D3D9. Piense también en trasladar a 64 bits, ya que esto se hará más frecuente en el futuro.

</dd> </dl>

## <a name="predicated-rendering"></a>Representación de predicado

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>He usado la representación predicada (basada en los resultados de la consulta de oclusión). ¿Por qué la aplicación sigue siendo la misma velocidad? 
</dt> <dd>

En primer lugar, asegúrese de que la representación que desea omitir es realmente el cuello de botella de la aplicación. Si no es el cuello de botella, omitir la representación no ayudará a la velocidad de fotogramas.

En segundo lugar, asegúrese de que ha transcurrido el tiempo suficiente entre el problema de la consulta y la representación que desea predicar. Si la consulta no ha finalizado en el momento en que la llamada de representación alcanza la GPU, se producirá la representación de todos modos.

En tercer lugar, predication solo omite ciertas llamadas. Las llamadas que se omiten son Draw, Clear, Copy, Update, ResolveSubresource y GenerateMips. La configuración de estado, la configuración de IA, la asignación y las llamadas de creación no respetan predication. Si hay una gran cantidad de llamadas de configuración de estado alrededor de la llamada a Draw que se va a predicar, estos Estados se establecerán.

</dd> </dl>

## <a name="geometry-shader"></a>Sombreador de geometría

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>¿Debo usar el sombreador de geometría para dividirlasr mi (insertar algo aquí)? 
</dt> <dd>

No. El sombreador de geometría no se debe utilizar para la teselación.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>¿Puedo usar el sombreador de geometría para crear geometría? 
</dt> <dd>

Sí, en escenarios muy limitados. El sombreador de geometría en las partes actuales de D3D10 (2008) no está equipado para controlar la gran expansión. Esto puede cambiar en el futuro. Los proveedores de tarjetas de vídeo pueden tener una ruta de acceso especial para una o cuatro expansiones debido a un hardware de punto y Sprite existente. Cualquier otra expansión tendría que ser muy limitada. Los ejemplos de ParticlesGS y PipesGS logran velocidades de fotogramas altas al realizar solo una expansión limitada. Solo se expanden unos cuantos puntos por fotograma.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>¿Para qué se debe usar el sombreador de geometría? 
</dt> <dd>

Cualquier elemento que requiera operaciones en un primitivo completo, como la detección de siluetas, las coordenadas Barycentric, etc. Úselo también para seleccionar el segmento de una matriz de destino de representación a la que se van a enviar primitivos.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>¿Se pueden generar cantidades variables de geometría desde el sombreador de geometría? 
</dt> <dd>

Sí, pero esto puede causar problemas de rendimiento. Tome el ejemplo de salida de 1 punto para una invocación y 4 puntos para otro. Al ajustarse dentro de las instrucciones de expansión, esto puede hacer que los subprocesos del sombreador de geometría se ejecuten en serie.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>¿Cómo D3D10 sabe cómo generar índices de adyacencia para mi malla? O, ¿por qué D3D10 no se representa correctamente cuando se especifica que el sombreador de geometría necesita información de adyacencia. 
</dt> <dd>

D3D10 no crea la información de adyacencia, sino que la aplicación. La aplicación genera índices de adyacencia y debe contener seis índices por primitivo; de los seis, los índices con números impares son los vértices adyacentes del borde. ID3DX10Mesh:: GenerateAdjacencyAndPointsReps se puede usar para generar estos datos.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>¿Son lentas las instrucciones de tipo entero y bit a bit? 
</dt> <dd>

Pueden ser. Varias tarjetas D3D10 solo pueden emitir operaciones de enteros en un subconjunto de las unidades de ALU disponibles. Esto depende en gran medida del hardware. Consulte a su proveedor de hardware individual para obtener recomendaciones sobre cómo abordar las operaciones de enteros en ese hardware determinado. Además, preste mucha atención a las conversiones entre tipos.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>¿Qué ha ocurrido con VPOS? 
</dt> <dd>

Si declara una entrada en el sombreador de píxeles como posición de la VP \_ , obtendrá el mismo comportamiento que la declaración como VPOS.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Cómo muestra una textura de MSAA? 
</dt> <dd>

En el sombreador, declare la textura como Texture2DMS. A continuación, puede capturar ejemplos individuales con los métodos de ejemplo fuera del objeto Texture2DMS.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Cómo saber si se usa realmente una variable de sombreador en un búfer de constantes? 
</dt> <dd>

Fíjese en el \_ struct de la variable de sombreador D3D10 reflejada \_ \_ para esa variable. uFlags debe tener establecido el \_ indicador D3D10 SVF \_ used.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Cómo saber si una variable de sombreador en un búfer de constantes está usando FX10? 
</dt> <dd>

Actualmente no es posible usar FX10.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>No tengo ningún control sobre los búferes de constantes que crea FX10. ¿Cómo se crean y actualizan? 
</dt> <dd>

Todos los búferes de constantes administrados por FX10 se crean como \_ \_ recursos predeterminados de uso de D3D10 y se actualizan con UpdateSubresource. Dado que FX10 mantiene una memoria auxiliar de todos los datos constantes, UpdateSubresource es el mejor enfoque para actualizarlos.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Cómo emular la canalización de funciones fijas mediante sombreadores? 
</dt> <dd>

Vea el ejemplo FixedFuncEMU.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>¿Debo usar las nuevas \[ sugerencias de \] \[ \] \[ compilador, bucle, bifurcación, \] etc.? 
</dt> <dd>

En general, no. El compilador probará a menudo ambos modos y elegirá el más rápido. En algunos casos, puede ser necesario utilizar \[ unroll \] , por ejemplo, cuando una captura de textura dentro de un bucle necesita tener acceso a un degradado.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>¿La precisión parcial marca una diferencia en D3D10? Puedo especificar una precisión parcial en el HLSL D3D9, pero no en mi D3D10 HLSL. 
</dt> <dd>

Todas las operaciones de D3D10 se especifican para ejecutarse en una precisión de punto flotante de 32 bits. Por lo tanto, la precisión parcial no debe hacer ninguna diferencia en D3D10.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>En D3D9, podía realizar el filtrado de sombra PCF de HW enlazando un búfer de profundidad como textura y usando las instrucciones de HLSL tex2d normales. Cómo hacer esto en D3D10? 
</dt> <dd>

Tiene que usar un estado de muestra de comparación y usar instrucciones de SampleCmp.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>¿Cómo funciona esta palabra clave Register en D3D10? 
</dt> <dd>

La palabra clave Register de D3D10 se aplica ahora a la ranura a la que está enlazado un recurso determinado. En este caso, el recurso puede ser un búfer (constante o de otro tipo), una textura o una muestra.

-   En el caso de los búferes de constantes, use la sintaxis: Register (bN), donde N es la ranura de entrada (0-15)
-   En el caso de las texturas, use la sintaxis: Register (tN), donde N es la ranura de entrada (0-127)
-   En el caso de los muestreadores, use la sintaxis: Register (sN), donde N es la ranura de entrada (0-127)

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Cómo colocar una variable dentro de un búfer de constantes si Register solo se usa para especificar dónde se debe enlazar todo el búfer. 
</dt> <dd>

Use la palabra clave packoffset. El argumento para packoffset tiene el formato c \[ 0-4095 \] . \[ x, y, z, w \] . Por ejemplo:

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

En este búfer de constantes, IWaste2Floats se coloca en el tercer Float (12 bytes) en el búfer de constantes. IWasteMore se coloca en el decimotercer FLOAT4 o 52nd Float en el búfer de constantes.

</dd> </dl>

 

 