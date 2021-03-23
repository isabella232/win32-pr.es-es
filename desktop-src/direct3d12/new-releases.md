---
title: Novedades de Direct3D 12
description: En este tema se describe la nueva documentación de Direct3D 12 más significativa disponible para varias versiones.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549061"
---
# <a name="whats-new-in-direct3d-12"></a>Novedades de Direct3D 12

En este tema se describe la nueva documentación de Direct3D 12 más significativa disponible para varias versiones.

Para obtener información sobre cómo obtener e instalar Direct3D, vea [configuración del entorno de programación de Direct3D 12](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 en Windows 7

- [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) ya está disponible para que lo usen los desarrolladores.

## <a name="windows-10-may-2019-update"></a>Actualización del 10 de mayo de 2019 de Windows 2019

Estas características y API se agregaron o actualizaron para Windows 10, versión 1903 (10,0; Compilación 18362) &mdash; también conocida como Windows 10 mayo de actualización de 2019.

- [Sombreado de velocidad variable (VRS)](./vrs.md). Permite asignar potencia y rendimiento de la representación que varían en la imagen representada.
- [Modelo de sombreador de HLSL 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4.
- Enumeración [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) . Define constantes que especifican una versión de los datos extendidos quitados del dispositivo (DRED).
- [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) estructura. Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos.
- [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) estructura. Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos.
- Enumeración [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Define constantes que especifican un nivel de tasa de sombreado (para el sombreado de velocidad variable o VRS).
- Interfaz [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) y sus métodos. Se utiliza para establecer el modo de optimización del procesamiento en segundo plano del controlador. Vea también [optimizaciones del sombreador de fondo](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- Interfaz [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) y sus métodos. Proporciona acceso en tiempo de ejecución a los datos de los datos extendidos (DRED) quitados del dispositivo.
- Interfaz [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) y sus métodos. Controla el dispositivo quitó la configuración de datos extendidos (DRED).
- Interfaz [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) y sus métodos. Compatibilidad con el sombreado de velocidad variable (VRS).

La enumeración de [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) se ha actualizado con la adición de la constante **D3D_SHADER_MODEL_6_5** (una característica de nivel experimental).

La enumeración de [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) se ha actualizado con la adición de la constante **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** .

La enumeración de [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) se ha actualizado con la adición de las constantes **D3D12_FEATURE_D3D12_OPTIONS6** y **D3D12_FEATURE_QUERY_META_COMMAND** .

La enumeración de [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) se ha actualizado con la adición de la constante **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** .

## <a name="windows-10-version-1809"></a>Windows 10, versión 1809

Estas características y API se agregaron o actualizaron para Windows 10, versión 1809 (10,0; Compilación 17763) &mdash; también se conoce como actualización de Windows 10 de octubre de 2018.

- [Direct3D 12 raytracing](./direct3d-12-raytracing.md)
- [Fases de representación de Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

Estas interfaces se han agregado a la documentación de Direct3D para Windows 10, versión 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) amplía la funcionalidad de creación de vallas, ya que admite la recuperación de marcas pasadas para crear la barrera.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) extiende la lista de comandos de gráficos disponibles al permitir escribir valores inmediatos directamente en un búfer.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) extiende la funcionalidad del adaptador virtual mediante la creación de montones de diagnóstico de propósito especial en la memoria del sistema que se conservan incluso en caso de que se produzca un escenario de error de GPU o de dispositivo quitado.

La enumeración del [**\_ \_ modelo de sombreador D3D**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) tiene un nuevo valor del **\_ sombreador de D3D \_ \_ \_** que se ha agregado para describir el modelo de sombreador 6,1.

La enumeración de [**\_ características de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) también tiene la nueva **característica de D3D12 \_ \_ D3D12 \_ OPTIONS3** y **D3D12 características de los \_ \_ \_ montones existentes** . Como los nombres implican, estos valores le permiten buscar opciones adicionales de Direct3D12, así como comprobar la compatibilidad de los montones existentes.

## <a name="windows-10-version-1703"></a>Windows 10, versión 1703

Estos temas se han agregado a la documentación de Direct3D para Windows 10, versión 1703.

-   El método [**ID3D12Device2:: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) y el struct de estado de canalización D3D12 de la estructura DESC representan una forma nueva y más robusta de crear PSO y unifica la [**\_ \_ \_ intercadenación \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) para crear canalizaciones de gráficos y de proceso.
-   El método [**ID3D12Device1:: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) expande la interfaz de la biblioteca de canalizaciones para aceptar el PSO creado con la nueva estructura de [**secuencia de \_ Estado de canalización \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) unificada.
-   La función [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) permite a los desarrolladores experimentar con ciertas características en desarrollo mediante una máquina en modo de programador.
-   Hay cinco interfaces nuevas (consulte la jerarquía de la [interfaz](interface-hierarchy.md)):
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Consulte la [información general del modelo de sombreador de HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), que describe las operaciones intrínsecas de onda para los sombreadores de cálculo y píxel multiproceso.
-   El uso de [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) ha cambiado.
-   Algunas de las nuevas características de Direct3D 11 se describen en [características de direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) y [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) habilitan **el bloqueo temporal** para reducir la latencia de pervieved.
-   [**ID3D12Device2:: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) y [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) habilitan las **pruebas de límites de profundidad en el** hardware compatible.
-   [**ResolveSubresourceRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) habilita la **resolución parcial** de Subrecursos para ayudar a optimizar el rendimiento.
-   [**SetSamplePositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) habilita las **posiciones de ejemplo programables** en el hardware compatible.

## <a name="november-2016-documentation-update"></a>Actualización de la documentación de noviembre de 2016

-   Revisión de los comentarios de [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Aclaración de "caída del estado a común" (vea [uso de barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   El archivo de encabezado D3dx12. h, al que se hace referencia en las [estructuras y funciones auxiliares de D3D12](helper-structures-and-functions-for-d3d12.md), se puede descargar directamente desde [la biblioteca auxiliar de D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).

## <a name="august-2016-documentation-update-2"></a>Actualización 2 de la documentación de agosto de 2016

-   Una nueva sección de la guía titulada [comprender la capa de depuración D3D12](understanding-the-d3d12-debug-layer.md).

    Se describen tres nuevas interfaces de la capa de depuración (en modo de vista previa): [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Actualización 1 de la documentación de agosto de 2016

-   Revisión del [uso de barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Revisión del [acceso a los recursos de varias colas](./user-mode-heap-synchronization.md#multi-queue-resource-access).

## <a name="windows-10-version-1607"></a>Windows 10, versión 1607

Estos temas se han agregado a la documentación de Direct3D para Windows 10, versión 1607.

-   [Firma raíz versión 1,1](root-signature-version-1-1.md) : información general de las firmas raíz actualizadas, que permiten a las aplicaciones especificar cómo los datos y los descriptores estáticos o volátiles son, lo que puede ayudar a las optimizaciones del controlador de gráficos.
-   El método [**ID3D12Device1:: CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) describe las ventajas de la creación de una biblioteca de canalizaciones.
-   Hay tres interfaces nuevas (consulte la jerarquía de la [interfaz](interface-hierarchy.md)):
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Consulte la [información general del modelo de sombreador de HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), que describe las operaciones intrínsecas de onda para los sombreadores de cálculo y píxel multiproceso.
-   El uso de [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) ha cambiado.
-   Algunas de las nuevas características de Direct3D 11 se describen en [características de direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   El intervalo de bibliotecas admitidas para Direct3D 12 se ha actualizado, consulte la sección **herramientas y bibliotecas compatibles** de [configuración del entorno de programación de Direct3D 12](directx-12-programming-environment-set-up.md).
-   [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md)
-   [Se muestra la frecuencia de actualización de variables](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Mejoras en DXGI 1,5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)