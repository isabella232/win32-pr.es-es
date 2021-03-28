---
title: Características de Direct3D 11,1
description: La siguiente funcionalidad se ha agregado en Direct3D 11,1, que se incluye con Windows 8, Windows RT y Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791770"
---
# <a name="direct3d-111-features"></a>Características de Direct3D 11,1

La siguiente funcionalidad se ha agregado en Direct3D 11,1, que se incluye con Windows 8, Windows RT y Windows Server 2012. La compatibilidad parcial con [Direct3D 11,1](direct3d-11-features.md) está disponible en Windows 7 y windows Server 2008 R2 a través de la [actualización de la plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponible a través de la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838).

-   [Seguimiento del sombreador y mejoras del compilador](#shader-tracing-and-compiler-enhancements)
-   [Uso compartido de dispositivos Direct3D](#direct3d-device-sharing)
-   [Comprobar la compatibilidad de las nuevas características y formatos de Direct3D 11,1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Usar precisión mínima de HLSL](#use-hlsl-minimum-precision)
-   [Especificar los planos de clip de usuario en HLSL en el nivel de característica 9 y versiones posteriores](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Crear búferes de constantes más grandes de los que puede tener acceso un sombreador](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Usar operaciones lógicas en un destino de representación](#use-logical-operations-in-a-render-target)
-   [Forzar el recuento de muestras para crear un estado de rasterizador](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Procesamiento de recursos de vídeo con sombreadores](#process-video-resources-with-shaders)
-   [Compatibilidad ampliada con recursos compartidos de Texture2D](#extended-support-for-shared-texture2d-resources)
-   [Cambiar Subrecursos con nuevas opciones de copia](#change-subresources-with-new-copy-options)
-   [Descartar recursos y vistas de recursos](#discard-resources-and-resource-views)
-   [Compatibilidad con un número mayor de UAVs](#support-a-larger-number-of-uavs)
-   [Enlazar un subintervalo de un búfer de constantes a un sombreador](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperar el subintervalo de un búfer de constantes que está enlazado a un sombreador](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Borrar todo o parte de una vista de recursos](#clear-all-or-part-of-a-resource-view)
-   [Asignación de SRVs de búferes dinámicos sin \_ sobrescritura](/windows)
-   [Usar UAVs en cada fase de canalización](#use-uavs-at-every-pipeline-stage)
-   [Compatibilidad ampliada con dispositivos dewarps](#extended-support-for-warp-devices)
-   [Usar Direct3D en procesos de sesión 0](#use-direct3d-in-session-0-processes)
-   [Compatibilidad con el búfer de sombra en el nivel de característica 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Temas relacionados](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Seguimiento del sombreador y mejoras del compilador

Direct3D 11,1 le permite usar el seguimiento del sombreador para asegurarse de que el código funciona según lo previsto y, si no es así, puede detectar y remediar el problema. El kit de desarrollo de software (SDK) de Windows para Windows 8 contiene mejoras del compilador de HLSL. El seguimiento del sombreador y el compilador de HLSL se implementan en D3dcompiler \_nn.dll.

La API de seguimiento del sombreador y las mejoras del compilador de HLSL se componen de los siguientes métodos y funciones.

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

La biblioteca D3dcompiler. lib requiere D3dcompiler \_nn.dll. Este archivo DLL no forma parte de Windows 8; está en la \\ carpeta bin de la Windows SDK para Windows 8 junto con la versión de línea de comandos Fxc.exe del compilador de HLSL.

> [!Note]  
> Aunque puede usar esta combinación de biblioteca y DLL para el desarrollo, no puede implementar aplicaciones de la tienda Windows que usen esta combinación. Por lo tanto, debe compilar sombreadores HLSL antes de enviar la aplicación de la tienda Windows. Puede escribir archivos binarios de compilación de HLSL en el disco o el compilador puede generar encabezados con matrices de bytes estáticas que contengan los datos del BLOB del sombreador. La interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) se usa para tener acceso a los datos del BLOB. Para desarrollar la aplicación de la tienda Windows, llame a [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) o [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) para compilar el origen HLSL sin formato y, a continuación, inserte los datos BLOB resultantes en Direct3D.

 

## <a name="direct3d-device-sharing"></a>Uso compartido de dispositivos Direct3D

Direct3D 11,1 habilita las API de Direct3D 10 y las API de Direct3D 11 para usar un dispositivo de representación subyacente.

Esta característica de Direct3D 11,1 consta de los siguientes métodos e interfaz.

-   [**ID3D11Device1:: CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1:: SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Comprobar la compatibilidad de las nuevas características y formatos de Direct3D 11,1

Direct3D 11,1 le permite comprobar si hay nuevas características compatibles con el controlador de gráficos y las nuevas maneras en que se admite un formato en un dispositivo. Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 también especifica nuevos valores de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ datos de \_ características \_ D3D11 \_ Opciones de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ \_ \_ \_ información de arquitectura de datos de características**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**D3D11 \_ \_ \_ \_ Opciones de D3D9**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)de datos de características, [**D3D11 \_ \_ \_ \_ \_ \_ compatibilidad de precisión mínima del sombreador de datos de características**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)y [**D3D11 datos de características D3D9 estructuras de \_ \_ \_ \_ \_ compatibilidad con instantáneas**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support)
-   [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) con [**\_ formato D3D11 \_ admite la \_ \_ salida del descodificador**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), el [**formato D3D11 de la \_ \_ \_ \_ \_ salida del procesador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), el formato de D3D11 de [**\_ \_ \_ \_ \_ entrada del procesador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), el formato de [**D3D11 \_ \_ \_ \_ codificador de vídeo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)y el formato de [**D3D11 lógica de \_ \_ combinación de \_ salida \_ \_ \_ del cliente2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Usar precisión mínima de HLSL

A partir de Windows 8, los controladores de gráficos pueden implementar [tipos de datos escalares HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) de precisión mínima con cualquier precisión mayor o igual que la precisión de bits especificada. Cuando el código del sombreador de precisión mínima de HLSL se usa en hardware que implementa la precisión mínima de HLSL, se usa menos ancho de banda de memoria y, como resultado, también se usa menos energía del sistema.

Puede consultar la compatibilidad de precisión mínima que proporciona el controlador de gráficos llamando a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con el valor de [**\_ \_ \_ \_ \_ compatibilidad de precisión mínima del sombreador de características de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . En esta llamada a **ID3D11Device:: CheckFeatureSupport** , se pasa un puntero a una estructura de [**\_ \_ \_ \_ \_ \_ compatibilidad de precisión mínima del sombreador de datos de característica de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) que **ID3D11Device:: CheckFeatureSupport** rellena con los niveles de precisión mínimos que admite el controlador para la etapa del sombreador de píxeles y para otras fases del sombreador. La información devuelta solo indica que el hardware gráfico puede realizar operaciones de HLSL con una precisión inferior a la precisión de punto flotante de 32 bits estándar, pero no garantiza que el hardware gráfico se ejecute realmente con una precisión inferior.

No es necesario crear varios sombreadores que no utilicen la precisión mínima. En su lugar, cree sombreadores con precisión mínima y las variables de precisión mínima se comportan en una precisión completa de 32 bits si el controlador de gráficos informa de que no admite ninguna precisión mínima. Para obtener más información sobre la precisión mínima de HLSL, consulte uso de la [precisión mínima de HLSL](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

Los sombreadores de precisión mínima de HLSL no funcionan en sistemas operativos anteriores a Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Especificar los planos de clip de usuario en HLSL en el nivel de característica 9 y versiones posteriores

A partir de Windows 8, puede usar el atributo de función **clipplanes** en una [declaración de función](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) HLSL en lugar de la [VP \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) para que el sombreador funcione en el [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 9 x, así como en el \_ nivel de característica 10 y versiones posteriores. Para obtener más información, consulte [planos de clips de usuario en hardware de nivel de característica 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Crear búferes de constantes más grandes de los que puede tener acceso un sombreador

Direct3D 11,1 le permite crear búferes de constantes que son mayores que el tamaño de búfer constante máximo al que puede tener acceso un sombreador (4096 32-bit \* 4-constantes de componente – 64 KB). Más adelante, al enlazar los búferes a la canalización, por ejemplo, a través de [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) o [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), puede especificar un intervalo de búferes al que el sombreador pueda tener acceso y que quepa dentro del límite de 4096.

Direct3D 11,1 actualiza el método [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) para esta característica.

## <a name="use-logical-operations-in-a-render-target"></a>Usar operaciones lógicas en un destino de representación

Direct3D 11,1 le permite usar operaciones lógicas en lugar de mezclar en un destino de representación. Sin embargo, no se pueden mezclar operaciones de lógica con la combinación entre varios destinos de representación.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) con la [ **lógica de D3D11 \_ \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forzar el recuento de muestras para crear un estado de rasterizador

Direct3D 11,1 le permite especificar un recuento de muestras de fuerza al crear un estado de rasterizador.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Si desea representar con el recuento de muestras forzado a 1 o superior, debe seguir estas instrucciones:
>
> -   No enlazar vistas de la galería de símbolos de profundidad.
> -   Deshabilite las pruebas de profundidad.
> -   Asegúrese de que el sombreador no genera profundidad.
> -   Si tiene alguna vista de destino de representación enlazada [**( \_ \_ \_ destino de representación de enlace de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) y forzó el recuento de muestras a un número mayor que 1, asegúrese de que cada destino de representación tiene solo un único ejemplo.
> -   No use el sombreador en la frecuencia de ejemplo. Por lo tanto, [**ID3D11ShaderReflection:: IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) devuelve **false**.
>
> De lo contrario, el comportamiento de representación es indefinido. Para obtener información sobre cómo configurar la característica de estarcido de profundidad, consulte Configuración de la [funcionalidad de Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Procesamiento de recursos de vídeo con sombreadores

Direct3D 11,1 le permite crear vistas (SRV/RTV/UAV) en recursos de vídeo para que los sombreadores de Direct3D puedan procesar esos recursos de vídeo. El formato de un recurso de vídeo subyacente restringe los formatos que puede usar la vista. La enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contiene nuevos valores de formato de recurso de vídeo. Estos valores de **\_ formato de DXGI** especifican los formatos de vista válidos que se pueden crear y el modo en que el tiempo de ejecución de Direct3D 11,1 asigna la vista. Puede crear varias vistas de distintas partes de la misma superficie y, según el formato, los tamaños de las vistas pueden diferir entre sí.

Direct3D 11,1 actualiza los siguientes métodos para esta característica.

-   [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device:: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Compatibilidad ampliada con recursos compartidos de Texture2D

Direct3D 11,1 garantiza que puede compartir los recursos de Texture2D que creó con formatos y tipos de recursos concretos. Para compartir los recursos de Texture2D, use los recursos [**\_ \_ \_ compartidos varios**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)de recurso D3D11, D3D11 de recurso compartido de [**\_ \_ \_ \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), o una combinación de las marcas D3D11 de recurso **\_ \_ \_ compartido \_** de KEYEDMUTEX y [**D3D11 de \_ recurso \_ \_ compartido \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) de NTHANDLE (nuevo para Windows 8) cuando cree esos recursos.

Direct3D 11,1 garantiza que puede compartir los recursos de Texture2D que creó con estos valores de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM
-   Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM
-   Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM
-   Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM
-   Formato de DXGI \_ \_ R16G16B16A16 \_ float

Además, Direct3D 11,1 garantiza que puede compartir los recursos de Texture2D que creó con un nivel de mipmap de 1, el tamaño de matriz de 1, los marcadores de enlace del [**\_ \_ \_ recurso de sombreador de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) y el destino de representación de enlace de D3D11 combinados, el valor predeterminado de uso ([**\_ \_ valor predeterminado de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) y solo estos valores de [**\_ \_ \_ marca de varios recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) : [**\_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

-   [**\_Recurso \_ compartido D3D11 varios \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Recurso \_ compartido D3D11 \_ varios \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Recurso \_ compartido D3D11 \_ varios \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Recurso D3D11 \_ Misc \_ GDI \_ compatible**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11,1 le permite compartir una mayor variedad de formatos y tipos de recursos de Texture2D. Puede consultar si el controlador de gráficos y el hardware admiten el uso compartido de recursos Texture2D extendido mediante una llamada a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con el valor de [**\_ \_ \_ las opciones D3D11 de la característica D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . En esta llamada a **ID3D11Device:: CheckFeatureSupport** , pase un puntero a una estructura de [**\_ \_ \_ \_ Opciones D3D11 de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) . **ID3D11Device:: CheckFeatureSupport** establece el miembro **ExtendedResourceSharing** de **D3D11 \_ Feature \_ Data \_ D3D11 \_ Options** en **true** si el hardware y el controlador admiten el uso compartido de recursos de Texture2D extendido.

Si [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **true** en **ExtendedResourceSharing**, puede compartir los recursos creados con estos valores de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Formato de \_ DXGI \_ sin tipo R32G32B32A32
-   Formato de DXGI \_ \_ R32G32B32A32 \_ float
-   Formato de DXGI \_ \_ R32G32B32A32 \_ uint
-   Formato de DXGI \_ \_ R32G32B32A32 \_ Sint
-   \_Formato de \_ DXGI \_ sin tipo R16G16B16A16
-   Formato de DXGI \_ \_ R16G16B16A16 \_ float
-   Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM
-   Formato de DXGI \_ \_ R16G16B16A16 \_ uint
-   Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM
-   Formato de DXGI \_ \_ R16G16B16A16 \_ Sint
-   Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM
-   Formato de DXGI \_ \_ R10G10B10A2 \_ uint
-   \_Formato de \_ DXGI \_ sin tipo R8G8B8A8
-   Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM
-   Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ R8G8B8A8 \_ uint
-   Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM
-   Formato de DXGI \_ \_ R8G8B8A8 \_ Sint
-   \_Formato de \_ DXGI \_ sin tipo B8G8R8A8
-   Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM
-   Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM
-   Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato de \_ DXGI \_ sin tipo B8G8R8X8
-   Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Formato de \_ DXGI \_ sin tipo R32
-   Formato de DXGI \_ \_ R32 \_ float
-   Formato de DXGI \_ \_ R32 \_ uint
-   Formato de DXGI \_ \_ R32 \_ Sint
-   \_Formato de \_ DXGI \_ sin tipo R16
-   Formato de DXGI \_ \_ R16 \_ float
-   Formato de DXGI \_ \_ R16 \_ UNORM
-   Formato de DXGI \_ \_ R16 \_ uint
-   Formato de DXGI \_ \_ R16 \_ SNORM
-   Formato de DXGI \_ \_ R16 \_ Sint
-   Formato de DXGI \_ \_ R8 \_ sin tipo
-   Formato de DXGI \_ \_ R8 \_ UNORM
-   Formato de DXGI \_ \_ R8 \_ uint
-   Formato de DXGI \_ \_ R8 \_ SNORM
-   Formato de DXGI \_ \_ R8 \_ Sint
-   Formato de DXGI \_ \_ a8 \_ UNORM
-   formato de DXGI \_ \_ AYUV
-   Formato de DXGI \_ \_ YUY2
-   Formato de DXGI \_ \_ NV12
-   Formato de DXGI \_ \_ NV11
-   Formato de DXGI \_ \_ P016
-   Formato de DXGI \_ \_ P010
-   Formato de DXGI \_ \_ Y216
-   Formato de DXGI \_ \_ Y210
-   Formato de DXGI \_ \_ Y416
-   Formato de DXGI \_ \_ Y410

Si [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **true** en **ExtendedResourceSharing**, puede compartir los recursos que creó con estas características y marcas:

-   [**\_Valor predeterminado de uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**\_Recurso de \_ sombreador de enlace de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Destino de \_ representación de enlace de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**El \_ recurso D3D11 \_ varios \_ generan \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ enlazar el \_ acceso desordenado \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Niveles de mipmap (uno o más niveles) en los recursos de textura 2D (especificados en el miembro **MipLevels** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Matrices de recursos de textura 2D (una o más texturas) (especificadas en el miembro **tamaño** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**Descodificador de enlace de D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_ \_ \_ Contenido restringido de varios recursos de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**Recurso \_ \_ compartido D3D11 varios recursos \_ \_ compartidos \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Controlador de \_ \_ \_ recursos compartidos varios \_ \_ de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Cuando **ExtendedResourceSharing** es **true**, tiene más flexibilidad al especificar las marcas de enlace para compartir recursos de Texture2D. No solo el controlador de gráficos y el hardware admiten más marcas de enlace, sino también más combinaciones posibles de marcadores de enlace. Por ejemplo, puede especificar simplemente el [**\_ destino de \_ representación \_ de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) o no hay marcas de enlace, etc.

 

Incluso si [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **true** en **ExtendedResourceSharing**, todavía no se pueden compartir los recursos creados con estas características y marcas:

-   [**D3D11 \_ \_ Galería de símbolos de profundidad de enlace \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   recursos de textura 2D en el modo de suavizado de contorno de muestras múltiples (MSAA) (especificado con el ejemplo de la [**\_ \_ Descripción de DXGI**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**\_Abrazadera de \_ \_ recursos varios de recursos \_ de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USO \_ INmutable**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**uso de D3D11 \_ \_ dinámico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)o [**\_ \_ almacenamiento provisional de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (es decir, asignable)
-   [**D3D11 \_ recursos \_ varios \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Cambiar Subrecursos con nuevas opciones de copia

Direct3D 11,1 le permite usar nuevas marcas de copia para copiar y actualizar Subrecursos. Cuando se copia un subrecurso, los recursos de origen y de destino pueden ser idénticos y las regiones de origen y de destino pueden superponerse.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Descartar recursos y vistas de recursos

Direct3D 11,1 le permite descartar recursos y vistas de recursos del contexto del dispositivo. Esta nueva funcionalidad informa a la GPU de que ya no se necesita contenido existente en recursos o vistas de recursos.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Compatibilidad con un número mayor de UAVs

Direct3D 11,1 le permite usar un número mayor de UAVs al enlazar recursos a la [fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md) y al establecer una matriz de vistas para un recurso no ordenado.

Direct3D 11,1 actualiza los siguientes métodos para esta característica.

-   [**ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext:: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Enlazar un subintervalo de un búfer de constantes a un sombreador

Direct3D 11,1 le permite enlazar un subintervalo de un búfer de constantes para que un sombreador tenga acceso. Puede proporcionar un búfer de constantes mayor y especificar el subintervalo que puede usar el sombreador.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11DeviceContext1:: CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1:: GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1:: HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1:: VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperar el subintervalo de un búfer de constantes que está enlazado a un sombreador

Direct3D 11,1 le permite recuperar el subrango de un búfer de constantes que está enlazado a un sombreador.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11DeviceContext1:: CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1:: GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1:: HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1:: VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Borrar todo o parte de una vista de recursos

Direct3D 11,1 le permite borrar una vista de recursos (RTV, UAV o cualquier vista de vídeo de una superficie Texture2D). El mismo valor de color se aplica a todos los elementos de la vista.

Esta característica de Direct3D 11,1 consta de la siguiente API.

-   [**ID3D11DeviceContext1:: ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Asignación de SRVs de búferes dinámicos sin \_ sobrescritura

Direct3D 11,1 le permite asignar vistas de recursos de sombreador (SRV) de búferes dinámicos con D3D11 \_ map \_ WRITE \_ no \_ overwrite. Los tiempos de ejecución de Direct3D 11 y anteriores limitan la asignación a los búferes de vértices o índices.

Direct3D 11,1 actualiza el método [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) para esta característica.

## <a name="use-uavs-at-every-pipeline-stage"></a>Usar UAVs en cada fase de canalización

Direct3D 11,1 le permite usar las siguientes instrucciones del modelo de sombreador 5,0 en todas las fases del sombreador que se usaron previamente en sombreadores de cálculo y sombreadores de píxeles.

-   [DCL \_ UAV \_ con tipo](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [UAV de DCL \_ \_ sin formato](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [UAV de DCL \_ \_ estructurado](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ sin formato](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [LD \_ estructurado](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [LD \_ UAV \_ con tipo](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [almacenamiento \_ sin procesar](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [almacenamiento \_ estructurado](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [almacenar \_ UAV \_ con tipo](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [sincronizar \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Todas las Atomic atómicas e inmediatas (por ejemplo, [Atomic \_ y](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) y [IMM \_ Atomic \_ y](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11,1 actualiza los siguientes métodos para esta característica.

-   [**ID3D11DeviceContext:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext:: CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext:: CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Estas instrucciones existían en Direct3D 11,0 en PS \_ 5 \_ 0 y CS \_ 5 \_ 0. Dado que Direct3D 11,1 hace que UAVs esté disponible en todas las fases del sombreador, estas instrucciones están disponibles en todas las fases del sombreador.

Si pasa sombreadores compilados (VS/HS/DS/HS) que usan cualquiera de estas instrucciones a una función Create-Shader, como [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), en dispositivos que no admiten UAVs en cada fase (incluidos los controladores existentes que no están implementados con esta característica), se produce un error en la función Create-Shader. También se produce un error en la función Create-Shader si el sombreador intenta usar una ranura UAV más allá del conjunto de ranuras UAV que admite el hardware.

La UAVs a la que hacen referencia estas instrucciones se comparte en todas las fases de canalización. Por ejemplo, un UAV enlazado en la ranura 0 en la [fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md) está disponible en la ranura 0 a vs/HS/DS/GS/PS.

No se garantiza que los accesos a UAV que emita desde o a través de fases del sombreador que se ejecuten en un determinado dibujo \* () o que emita desde el sombreador de cálculo dentro de un envío \* () finalicen en el orden en el que los emitió. Pero todos los accesos de UAV finalizan al final de Draw \* () o Dispatch \* ().

## <a name="extended-support-for-warp-devices"></a>Compatibilidad ampliada con dispositivos dewarps

Direct3D 11,1 extiende la compatibilidad con los dispositivos [Dewarps](overviews-direct3d-11-devices-create-warp.md) , que se crean pasando el [**\_ tipo de controlador D3D \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

A partir de la compatibilidad con dispositivos Direct3D 11,1 WARP:

-   Todos los [niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) de Direct3D de 9,1 a 11,1
-   [Sombreadores de cálculo](direct3d-11-advanced-stages-compute-shader.md) y [teselación](direct3d-11-advanced-stages-tessellation.md)
-   Superficies compartidas. Es decir, puede compartir completamente las superficies entre los dispositivos de deformación, así como entre los dispositivos de deformación en distintos procesos.

Los dispositivos WARP no admiten estas características opcionales:

-   [duplica](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codificación o descodificación de vídeo](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [compatibilidad con el sombreador de precisión mínimo](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Cuando se ejecuta una máquina virtual (VM), Hyper-V, con la unidad de procesamiento de gráficos (GPU) deshabilitada o sin un controlador de pantalla, se obtiene un dispositivo de ALABEo cuyo nombre descriptivo es "adaptador de pantalla básico de Microsoft". Este dispositivo WARP puede ejecutar la experiencia completa de Windows, que incluye las aplicaciones DWM, Internet Explorer y tienda Windows. Este dispositivo WARP también admite la ejecución de aplicaciones heredadas que usan [DirectDraw](/windows/desktop/directdraw/directdraw) o la ejecución de aplicaciones que usan Direct3D 3 a Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Usar Direct3D en procesos de sesión 0

A partir de Windows 8 y Windows Server 2012, puede usar la mayoría de las API de Direct3D en los procesos de sesión 0.

> [!Note]  
> Estos resultados, ventanas, cadenas de intercambio y API relacionadas con la presentación no están disponibles en los procesos de la sesión 0 porque no se aplican al entorno de la sesión 0:
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Si llama a una de las API anteriores en un proceso de sesión 0, devolverá un [**error de DXGI \_ \_ no \_ \_ disponible actualmente**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Compatibilidad con el búfer de sombra en el nivel de característica 9

Use un subconjunto de características de búfer de Direct3D 10 \_ 0 + de sombra para implementar efectos de sombra en el [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Para obtener información sobre lo que debe hacer para implementar efectos de sombra en el nivel de característica 9 \_ x, vea [implementar búferes de sombra para el nivel de características 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 