---
title: Características de Direct3D 11.1
description: La siguiente funcionalidad se ha agregado en Direct3D 11.1, que se incluye con Windows 8, Windows RT y Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee5f4721a9f7ef7727539387603e839f36690ed5d4b6762121ceddefa0672ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535976"
---
# <a name="direct3d-111-features"></a>Características de Direct3D 11.1

La siguiente funcionalidad se ha agregado en Direct3D 11.1, que se incluye con Windows 8, Windows RT y Windows Server 2012. La compatibilidad parcial con [Direct3D 11.1](direct3d-11-features.md) está disponible en Windows 7 y Windows Server 2008 R2 a través de la actualización de plataforma [para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponible a través de la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

-   [Seguimiento del sombreador y mejoras del compilador](#shader-tracing-and-compiler-enhancements)
-   [Uso compartido de dispositivos Direct3D](#direct3d-device-sharing)
-   [Comprobar la compatibilidad con las nuevas características y formatos de Direct3D 11.1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Uso de la precisión mínima de HLSL](#use-hlsl-minimum-precision)
-   [Especificación de planos de recorte de usuario en HLSL en el nivel de característica 9 y superior](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Crear búferes constantes más grandes a los que puede tener acceso un sombreador](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Uso de operaciones lógicas en un destino de representación](#use-logical-operations-in-a-render-target)
-   [Forzar el recuento de muestras para crear un estado de rasterizador](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Procesar recursos de vídeo con sombreadores](#process-video-resources-with-shaders)
-   [Compatibilidad ampliada con recursos compartidos de Texture2D](#extended-support-for-shared-texture2d-resources)
-   [Cambio de los subrecursos con nuevas opciones de copia](#change-subresources-with-new-copy-options)
-   [Descartar recursos y vistas de recursos](#discard-resources-and-resource-views)
-   [Compatibilidad con un mayor número de UAV](#support-a-larger-number-of-uavs)
-   [Enlazar un subrango de un búfer constante a un sombreador](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperación del subrango de un búfer constante enlazado a un sombreador](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Borrar todo o parte de una vista de recursos](#clear-all-or-part-of-a-resource-view)
-   [Asignar SRV de búferes dinámicos con NO \_ OVERWRITE](/windows)
-   [Uso de UAV en cada fase de canalización](#use-uavs-at-every-pipeline-stage)
-   [Compatibilidad ampliada con dispositivos WARP](#extended-support-for-warp-devices)
-   [Uso de Direct3D en procesos de sesión 0](#use-direct3d-in-session-0-processes)
-   [Compatibilidad con el búfer de sombras en el nivel de característica 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Temas relacionados](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Seguimiento del sombreador y mejoras del compilador

Direct3D 11.1 le permite usar el seguimiento del sombreador para asegurarse de que el código funciona según lo previsto y, si no es así, puede detectar y solucionar el problema. El Windows Software Development Kit (SDK) para Windows 8 contiene mejoras del compilador HLSL. El seguimiento del sombreador y el compilador HLSL se implementan en D3dcompiler \_nn.dll.

La API de seguimiento del sombreador y las mejoras del compilador HLSL constan de los siguientes métodos y funciones.

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

La biblioteca D3dcompiler.lib requiere D3dcompiler \_nn.dll. Este archivo DLL no forma parte de Windows 8; se encuentra en la carpeta bin del SDK de Windows para Windows 8 junto con la Fxc.exe de línea de comandos del compilador \\ HLSL.

> [!Note]  
> Aunque puede usar esta combinación de biblioteca y DLL para el desarrollo, no puede implementar aplicaciones Windows Store que usan esta combinación. Por lo tanto, debe compilar en su lugar sombreadores HLSL antes de enviar la aplicación Windows Store. Puede escribir archivos binarios de compilación HLSL en el disco o el compilador puede generar encabezados con matrices de bytes estáticas que contienen los datos del blob del sombreador. Use la interfaz [**ID3DBlob para**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) acceder a los datos del blob. Para desarrollar la aplicación Windows Store, llame a [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) o D3DCompileFromFile para compilar el origen HLSL sin formato y, a continuación, feed the resulting blob data to Direct3D [**(D3DCompileFromFile)**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) para compilar el origen HLSL sin formato y, a continuación, alimentar los datos de blob resultantes en Direct3D.

 

## <a name="direct3d-device-sharing"></a>Uso compartido de dispositivos Direct3D

Direct3D 11.1 permite que las API de Direct3D 10 y las API de Direct3D 11 usen un dispositivo de representación subyacente.

Esta característica de Direct3D 11.1 consta de los siguientes métodos e interfaz.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Comprobar la compatibilidad con las nuevas características y formatos de Direct3D 11.1

Direct3D 11.1 le permite comprobar si hay nuevas características que el controlador de gráficos pueda admitir y nuevas formas de admitir un formato en un dispositivo. Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.2 también especifica nuevos [**valores DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Esta característica de Direct3D 11.1 consta de la siguiente API.

-   [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info) [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ OPTIONS,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options) [**D3D11 \_ FEATURE DATA SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)y [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) structures
-   [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) with [**D3D11 \_ FORMAT SUPPORT DECODER \_ \_ \_ OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 FORMAT SUPPORT \_ VIDEO PROCESSOR \_ \_ \_ \_ OUTPUT,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support) [**D3D11 FORMAT SUPPORT VIDEO PROCESSOR \_ \_ \_ \_ \_ INPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO \_ \_ \_ ENCODER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)y [**D3D11 \_ FORMAT \_ SUPPORT2 OUTPUT MERGER LOGIC \_ \_ \_ \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Uso de la precisión mínima de HLSL

A partir Windows 8, los controladores gráficos pueden implementar tipos de datos [escalares HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) de precisión mínima mediante cualquier precisión mayor o igual que su precisión de bits especificada. Cuando el código del sombreador de precisión mínima HLSL se usa en hardware que implementa la precisión mínima hlsl, se usa menos ancho de banda de memoria y, como resultado, también se usa menos potencia del sistema.

Puede consultar la compatibilidad de precisión mínima que proporciona el controlador de gráficos llamando a [**ID3D11Device::CheckFeatureSupport con**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) el valor [**D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ SUPPORT.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) En esta llamada **ID3D11Device::CheckFeatureSupport,** pase un puntero a una estructura [**D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) que **ID3D11Device::CheckFeatureSupport** rellena con los niveles de precisión mínimos que admite el controlador para la fase del sombreador de píxeles y para otras fases del sombreador. La información devuelta solo indica que el hardware gráfico puede realizar operaciones HLSL con una precisión inferior a la precisión float estándar de 32 bits, pero no garantiza que el hardware gráfico se ejecute realmente con una precisión inferior.

No es necesario crear varios sombreadores que usen y no usen la precisión mínima. En su lugar, cree sombreadores con precisión mínima y las variables de precisión mínima se comporten con una precisión completa de 32 bits si el controlador de gráficos informa de que no admite ninguna precisión mínima. Para obtener más información sobre la precisión mínima de HLSL, vea [Using HLSL minimum precision](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

Los sombreadores de precisión mínima HLSL no funcionan en sistemas operativos anteriores a Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Especificación de planos de recorte de usuario en HLSL en el nivel de característica 9 y superior

A partir de Windows 8, puede usar el atributo de función [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) **clipplanes** en una declaración de función HLSL en lugar de [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) para que el sombreador funcione en el nivel [de](overviews-direct3d-11-devices-downlevel-intro.md) característica 9 x, así como en el nivel de característica \_ 10 y superior. Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Crear búferes constantes más grandes a los que puede tener acceso un sombreador

Direct3D 11.1 permite crear búferes constantes que son mayores que el tamaño máximo de búfer constante al que un sombreador puede acceder (4096 constantes de 32 bits de 4 componentes \* : 64 KB). Más adelante, al enlazar los búferes a la canalización, por ejemplo, a través de [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) o [**PSSetConstantBuffers1,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)puede especificar un intervalo de búferes a los que el sombreador puede acceder que se ajuste al límite 4096.

Direct3D 11.1 actualiza el [**método ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) para esta característica.

## <a name="use-logical-operations-in-a-render-target"></a>Uso de operaciones lógicas en un destino de representación

Direct3D 11.1 permite usar operaciones lógicas en lugar de combinar en un destino de representación. Sin embargo, no se pueden mezclar operaciones lógicas con la combinación entre varios destinos de representación.

Esta característica de Direct3D 11.1 consta de la siguiente API.

-   [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) con [ **D3D11 \_ LOGIC \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forzar el recuento de muestras para crear un estado de rasterizador

Direct3D 11.1 permite especificar un recuento de muestras de fuerza al crear un estado de rasterizador.

Esta característica de Direct3D 11.1 consta de la siguiente API.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Si desea representar con el recuento de muestras forzado a 1 o superior, debe seguir estas instrucciones:
>
> -   No enlace vistas de galería de símbolos de profundidad.
> -   Deshabilite las pruebas de profundidad.
> -   Asegúrese de que el sombreador no genera profundidad de salida.
> -   Si tiene vistas de destino de representación enlazadas [**(D3D11 \_ BIND \_ RENDER \_ TARGET)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)y ha forzado el recuento de muestras a mayor que 1, asegúrese de que cada destino de representación tiene solo una muestra.
> -   No utilice el sombreador con frecuencia de muestra. Por lo [**tanto, ID3D11ShaderReflection::IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) devuelve **FALSE**.
>
> De lo contrario, el comportamiento de representación es indefinido. Para obtener información sobre cómo configurar la galería de símbolos de profundidad, vea [Configuring Depth-Stencil Functionality](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Procesar recursos de vídeo con sombreadores

Direct3D 11.1 permite crear vistas (SRV/RTV/UAV) en recursos de vídeo para que los sombreadores de Direct3D puedan procesar esos recursos de vídeo. El formato de un recurso de vídeo subyacente restringe los formatos que puede usar la vista. La [**enumeración DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contiene nuevos valores de formato de recursos de vídeo. Estos **valores DE \_ DXGI FORMAT** especifican los formatos de vista válidos que puede crear y cómo asigna la vista el entorno de ejecución de Direct3D 11.1. Puede crear varias vistas de diferentes partes de la misma superficie y, en función del formato, los tamaños de las vistas pueden diferir entre sí.

Direct3D 11.1 actualiza los métodos siguientes para esta característica.

-   [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Compatibilidad ampliada con recursos compartidos de Texture2D

Direct3D 11.1 garantiza que puede compartir recursos de Texture2D creados con determinados tipos de recursos y formatos. Para compartir recursos de Texture2D, use las marcas [**\_ \_ MISC \_ SHARED DE RECURSOS DE D3D11,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) [**D3D11 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)o una combinación de las marcas **\_ \_ MISC SHARED \_ \_ KEYEDMUTEX** y [**D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (novedad para Windows 8) al crear esos recursos.

Direct3D 11.1 garantiza que puede compartir los recursos de Texture2D que creó con estos [**valores \_ de DXGI FORMAT:**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT

Además, Direct3D 11.1 garantiza que puede compartir recursos texture2D que creó con un nivel mipmap de 1, tamaño de matriz de 1, marcas de enlace de [**D3D11 \_ BIND \_ SHADER \_ RESOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) y [**D3D11 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) combinados, usage default [**(D3D11 \_ USAGE \_ DEFAULT)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)y solo estos valores de MARCA MISC DE RECURSOS [**D3D11: \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

-   [**RECURSO D3D11 \_ \_ COMPARTIDO \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**ERROR DE CLAVE COMPARTIDA DE RECURSOS D3D11 \_ \_ \_ \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ SHARED \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**COMPATIBILIDAD CON \_ \_ GDI DE MISC DE RECURSOS \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11.1 permite compartir una mayor variedad de tipos y formatos de recursos texture2D. Puede consultar si el controlador de gráficos y el hardware admiten el uso compartido extendido de recursos texture2D llamando a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con el valor [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) En esta **llamada ID3D11Device::CheckFeatureSupport,** pase un puntero a una estructura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) **ID3D11Device::CheckFeatureSupport** establece el miembro **ExtendedResourceSharing** de **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS** en **TRUE** si el hardware y el controlador admiten el uso compartido extendido de recursos texture2D.

Si [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **TRUE** en **ExtendedResourceSharing,** puede compartir los recursos que creó con estos [**valores DE FORMATO \_ DXGI:**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   FORMATO DXGI \_ \_ R32G32B32A32 \_ SIN TIPO
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ SINT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ TYPELESS
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UINT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ TYPELESS
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ SINT
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ TYPELESS
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ TYPELESS
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R32 \_ TYPELESS
-   DXGI \_ FORMAT \_ R32 \_ FLOAT
-   DXGI \_ FORMAT \_ R32 \_ UINT
-   DXGI \_ FORMAT \_ R32 \_ SINT
-   DXGI \_ FORMAT \_ R16 \_ TYPELESS
-   DXGI \_ FORMAT \_ R16 \_ FLOAT
-   DXGI \_ FORMAT \_ R16 \_ UNORM
-   DXGI \_ FORMAT \_ R16 \_ UINT
-   DXGI \_ FORMAT \_ R16 \_ SNORM
-   DXGI \_ FORMAT \_ R16 \_ SINT
-   DXGI \_ FORMAT \_ R8 \_ TYPELESS
-   DXGI \_ FORMAT \_ R8 \_ UNORM
-   DXGI \_ FORMAT \_ R8 \_ UINT
-   DXGI \_ FORMAT \_ R8 \_ SNORM
-   DXGI \_ FORMAT \_ R8 \_ SINT
-   DXGI \_ FORMAT \_ A8 \_ UNORM
-   FORMATO DXGI \_ \_ AYUV
-   DXGI \_ FORMAT \_ YUY2
-   FORMATO DXGI \_ \_ NV12
-   FORMATO DXGI \_ \_ NV11
-   DXGI \_ FORMAT \_ P016
-   DXGI \_ FORMAT \_ P010
-   DXGI \_ FORMAT \_ Y216
-   DXGI \_ FORMAT \_ Y210
-   DXGI \_ FORMAT \_ Y416
-   DXGI \_ FORMAT \_ Y410

Si [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **TRUE** en **ExtendedResourceSharing,** puede compartir los recursos que creó con estas características y marcas:

-   [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**RECURSO DE SOMBREADOR DE ENLACE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**DESTINO DE REPRESENTACIÓN DE ENLACE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**ERROR DE ASIGNACIÓN DE RECURSOS D3D11 \_ \_ \_ \_ GENERACIÓN DE MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ ENLAZAR \_ ACCESO \_ DESORDENADO**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Niveles mipmap (uno o varios niveles) en los recursos de textura 2D (especificados en el **miembro MipLevels** de [**D3D11 \_ TEXTURE2D \_ DESC)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)
-   Matrices de recursos de textura 2D (una o varias texturas) (especificadas en el miembro **ArraySize** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**DESCODIFICADOR DE ENLACE D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**CONTENIDO RESTRINGIDO CON ERRORES DE RECURSOS D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**RESTRICCIÓN DE RECURSOS \_ \_ COMPARTIDOS POR ERROR \_ \_ DE D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**ERROR DE USO DE RECURSOS D3D11 \_ \_ RESTRICT SHARED RESOURCE \_ \_ \_ \_ DRIVER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Cuando **ExtendedResourceSharing es** **TRUE,** tiene más flexibilidad al especificar marcas de enlace para compartir recursos de Texture2D. El controlador de gráficos y el hardware no solo admiten más marcas de enlace, sino también más combinaciones posibles de marcas de enlace. Por ejemplo, puede especificar solo [**D3D11 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) o ninguna marca de enlace, y así sucesivamente.

 

Incluso si [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) devuelve **TRUE** en **ExtendedResourceSharing,** todavía no puede compartir los recursos que creó con estas características y marcas:

-   [**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE ENLACE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Recursos de textura 2D en modo de suavizado de contorno de múltiples muestras (MSAA) (especificado con [**DXGI \_ SAMPLE \_ DESC)**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
-   [**FIJACIÓN DE RECURSOS \_ \_ MISC \_ DE RECURSOS D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USAGE \_ IMMUTABLE,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)o [**D3D11 \_ USAGE \_ STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (es decir, asignable)
-   [**RESOURCE \_ \_ MISC \_ TEXTURECUBE de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Cambio de los subrecursos con nuevas opciones de copia

Direct3D 11.1 permite usar nuevas marcas de copia para copiar y actualizar los subrecursos. Al copiar un subrecurso, los recursos de origen y destino pueden ser idénticos y las regiones de origen y destino se pueden superponer.

Esta característica de Direct3D 11.1 consta de la SIGUIENTE API.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Descartar recursos y vistas de recursos

Direct3D 11.1 permite descartar recursos y vistas de recursos del contexto del dispositivo. Esta nueva funcionalidad informa a la GPU de que ya no se necesita contenido existente en recursos o vistas de recursos.

Esta característica de Direct3D 11.1 consta de la SIGUIENTE API.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Compatibilidad con un mayor número de UAV

Direct3D 11.1 permite usar un mayor número de UAV al enlazar recursos a la fase de fusión de salida y al establecer una matriz de vistas para un recurso desordenado. [](d3d10-graphics-programming-guide-output-merger-stage.md)

Direct3D 11.1 actualiza los métodos siguientes para esta característica.

-   [**ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Enlazar un subrango de un búfer constante a un sombreador

Direct3D 11.1 permite enlazar un subrango de un búfer constante para que un sombreador acceda. Puede proporcionar un búfer constante mayor y especificar el subrango que puede usar el sombreador.

Esta característica de Direct3D 11.1 consta de la SIGUIENTE API.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperación del subrango de un búfer constante enlazado a un sombreador

Direct3D 11.1 permite recuperar el subrango de un búfer constante enlazado a un sombreador.

Esta característica de Direct3D 11.1 consta de la SIGUIENTE API.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Borrar todo o parte de una vista de recursos

Direct3D 11.1 permite borrar una vista de recursos (RTV, UAV o cualquier vista de vídeo de una superficie Texture2D). Aplique el mismo valor de color a todas las partes de la vista.

Esta característica de Direct3D 11.1 consta de la SIGUIENTE API.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Asignación de SRV de búferes dinámicos con NO \_ OVERWRITE

Direct3D 11.1 permite asignar vistas de recursos de sombreador (SRV) de búferes dinámicos con D3D11 \_ MAP \_ WRITE NO \_ \_ OVERWRITE. Direct3D 11 y los tiempos de ejecución anteriores limitaban la asignación a búferes de vértices o índices.

Direct3D 11.1 actualiza el [**método ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) para esta característica.

## <a name="use-uavs-at-every-pipeline-stage"></a>Uso de UAV en cada fase de canalización

Direct3D 11.1 permite usar las siguientes instrucciones del modelo de sombreador 5.0 en todas las fases del sombreador que se usaron anteriormente solo en sombreadores de píxeles y sombreadores de proceso.

-   [dcl \_ uav \_ con tipo](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [dcl \_ uav \_ raw](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [dcl \_ uav \_ structured](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [ld \_ raw](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [ld \_ structured](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [ld \_ uav \_ con tipo](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [store \_ raw](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [store \_ structured](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [store \_ uav \_ con tipo](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [sync \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Todos los atómicos y los atómicos inmediatos (por ejemplo, [atomic \_ y](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) [imm \_ atomic \_ y](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11.1 actualiza los métodos siguientes para esta característica.

-   [**ID3D11DeviceContext::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext::CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext::CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Estas instrucciones existían en Direct3D 11.0 en ps \_ 5 \_ 0 y cs \_ 5 \_ 0. Dado que Direct3D 11.1 hace que los UAV estén disponibles en todas las fases del sombreador, estas instrucciones están disponibles en todas las fases del sombreador.

Si pasa sombreadores compilados (VS/HS/DS/HS) que usan cualquiera de estas instrucciones a una función create-shader, como [**CreateVertexShader,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)en dispositivos que no admiten UAV en cada fase (incluidos los controladores existentes que no se implementan con esta característica), se produce un error en la función create-shader. También se produce un error en la función create-shader si el sombreador intenta usar una ranura UAV más allá del conjunto de ranuras UAV que admite el hardware.

Los UAV a los que hacen referencia estas instrucciones se comparten en todas las fases de canalización. Por ejemplo, un UAV enlazado en la [](d3d10-graphics-programming-guide-output-merger-stage.md) ranura 0 en la fase de fusión de salida está disponible en la ranura 0 a VS/HS/DS/GS/PS.

No se garantiza que los accesos UAV que se emiten desde dentro o entre las fases del sombreador que se ejecutan dentro de un draw determinado () o que se emiten desde el sombreador de proceso dentro de una distribución () finalicen en el orden en el que las \* \* emitió. Pero todos los accesos UAV finalizan al final de Draw \* () o Dispatch \* ().

## <a name="extended-support-for-warp-devices"></a>Compatibilidad ampliada con dispositivos WARP

Direct3D 11.1 amplía la compatibilidad con dispositivos [WARP,](overviews-direct3d-11-devices-create-warp.md) que se crean pasando [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* [**de D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

A partir de la compatibilidad con dispositivos WARP de Direct3D 11.1:

-   Todos los niveles de características [de](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D de 9.1 a 11.1
-   [Sombreadores de proceso](direct3d-11-advanced-stages-compute-shader.md) [y teselación](direct3d-11-advanced-stages-tessellation.md)
-   Superficies compartidas. Es decir, puede compartir completamente superficies entre dispositivos WARP, así como entre dispositivos WARP en distintos procesos.

Los dispositivos WARP no admiten estas características opcionales:

-   [Dobles](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codificación o descodificación de vídeo](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [compatibilidad con el sombreador de precisión mínima](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Al ejecutar una máquina virtual (VM), Hyper-V, con la unidad de procesamiento de gráficos (GPU) deshabilitada o sin un controlador de pantalla, obtiene un dispositivo WARP cuyo nombre descriptivo es "Adaptador de pantalla básico de Microsoft". Este dispositivo WARP puede ejecutar toda la experiencia Windows, que incluye DWM, Internet Explorer y Windows Store. Este dispositivo WARP también admite la ejecución de aplicaciones heredadas que usan [DirectDraw](/windows/desktop/directdraw/directdraw) o aplicaciones en ejecución que usan Direct3D 3 a Direct3D 11.1.

## <a name="use-direct3d-in-session-0-processes"></a>Uso de Direct3D en procesos de sesión 0

A partir Windows 8 y Windows Server 2012, puede usar la mayoría de las API de Direct3D en los procesos de la sesión 0.

> [!Note]  
> Estas API de salida, ventana, cadena de intercambio y relacionadas con la presentación no están disponibles en los procesos de la sesión 0 porque no se aplican al entorno de sesión 0:
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
> Si llama a una de las API anteriores en un proceso de sesión 0, devuelve [**DXGI \_ ERROR NOT CURRENTLY \_ \_ \_ AVAILABLE**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Compatibilidad con el búfer de sombras en el nivel de característica 9

Use un subconjunto de características de búfer de sombra de Direct3D 10 0+ para implementar efectos de sombra en el \_ nivel de característica 9 [](overviews-direct3d-11-devices-downlevel-intro.md) \_ x. Para obtener información sobre lo que debe hacer para implementar efectos de sombra en el nivel de característica 9 x, vea \_ [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))(Implementación de búferes de sombra para el nivel de característica 9 de Direct3D).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 