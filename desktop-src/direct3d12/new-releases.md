---
title: Novedades de Direct3D 12
description: En este tema se describe la nueva documentación más importante de Direct3D 12 disponible para varias versiones.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: 0ab45610eee3a2199fc91af639cee8175cc13030
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813089"
---
# <a name="whats-new-in-direct3d-12"></a>Novedades de Direct3D 12

En este tema se describe la nueva documentación más importante de Direct3D 12 disponible para varias versiones.

Para obtener información sobre cómo obtener e instalar Direct3D, vea Configuración del entorno de programación de [Direct3D 12.](./directx-12-programming-environment-set-up.md)

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 en Windows 7

- [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) ahora está disponible para que los desarrolladores los usen.

## <a name="windows-10-may-2019-update"></a>Actualización del 10 de mayo de 2019 de Windows 2019

Estas características y API se agregaron o actualizaron para Windows 10 versión 1903 (10.0; Compilación 18362) &mdash; también conocida como Actualización de mayo de 2019 de Windows 10.

- [Sombreado de velocidad variable (VRS).](./vrs.md) Le permite asignar rendimiento o potencia de representación a velocidades que varían en la imagen representada.
- [Modelo de sombreador HLSL 6.4.](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md) Describe los intrínsecos de aprendizaje automático agregados al modelo de sombreador HLSL 6.4.
- [**D3D12_DRED_VERSION enumeración.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) Define constantes que especifican una versión de Datos extendidos quitados del dispositivo (DRED).
- [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) estructura. Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos.
- [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) estructura. Indica el nivel de compatibilidad que proporciona el adaptador para los metacomandos.
- [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) enumeración. Define constantes que especifican un nivel de velocidad de sombreado (para el sombreado de velocidad variable o VRS).
- [**Interfaz ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) y sus métodos. Se usa para establecer el modo de optimizaciones de procesamiento en segundo plano del controlador. Consulte también [Optimizaciones del sombreador en segundo plano.](https://devblogs.microsoft.com/directx/background-shader-optimizations/)
- [**Interfaz ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) y sus métodos. Proporciona acceso en tiempo de ejecución a los datos de datos extendidos (DRED) quitados del dispositivo.
- [**Interfaz ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) y sus métodos. Controla la configuración de datos extendidos (DRED) quitados del dispositivo.
- [**Interfaz D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) y sus métodos. Compatibilidad con el sombreado de velocidad variable (VRS).

La [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) enumeración se ha actualizado con la adición de **la constante D3D_SHADER_MODEL_6_5** (una característica de nivel experimental).

La [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) enumeración se ha actualizado con la adición de **la D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** constante.

La [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) enumeración se ha actualizado con la adición de **D3D12_FEATURE_D3D12_OPTIONS6** y **D3D12_FEATURE_QUERY_META_COMMAND** constantes.

La [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeración se ha actualizado con la adición de **la D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** constante.

## <a name="windows-10-version-1809"></a>Windows 10, versión 1809

Estas características y API se agregaron o actualizaron para Windows 10, versión 1809 (10.0; Compilación 17763) &mdash; también conocida como Actualización de octubre de 2018 de Windows 10.

- [Direct3D 12 Raytracing](./direct3d-12-raytracing.md)
- [Pases de representación de Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

Estas interfaces se han agregado a la documentación de Direct3D Windows 10, versión 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) amplía la funcionalidad de creación de barreras al admitir la recuperación de las marcas pasadas para crear la barrera.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) amplía la lista de comandos gráficos disponibles al admitir la escritura de valores inmediatos directamente en un búfer.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) amplía la funcionalidad del adaptador virtual mediante la creación de montones de diagnóstico de uso especial en la memoria del sistema que persisten incluso en caso de un escenario de error de GPU o de dispositivo quitado.

La [**enumeración \_ D3D SHADER \_ MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) tiene un nuevo valor **D3D \_ SHADER MODEL \_ \_ 6 \_ 1** agregado para describir el modelo de sombreador 6.1.

La [**enumeración \_ FEATURE de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) también tiene los nuevos valores DE MONTÓN EXISTENTES DE CARACTERÍSTICAS **\_ D3D12 FEATURE \_ D3D12 \_ OPTIONS3** y **D3D12 \_ FEATURE \_ \_ EXISTING.** Como indican los nombres, estos valores le permiten buscar opciones adicionales de Direct3D12, así como comprobar la compatibilidad de los montones existentes.

## <a name="windows-10-version-1703"></a>Windows 10, versión 1703

Estos temas se han agregado a la documentación de Direct3D Windows 10, versión 1703.

-   El [**método ID3D12Device2::CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) y la estructura [**D3D12 \_ Pipeline State Stream \_ \_ \_ Desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) representan una manera nueva y más sólida de crear PSO y unifica el aspecto para crear canalizaciones de proceso y gráficos.
-   El [**método ID3D12Device1::CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) expande la interfaz de la biblioteca de canalizaciones para aceptar los PSO creados con la nueva estructura [**\_ \_ \_ \_ Desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) de flujo de estado de canalización D3D12 unificada.
-   La [**función D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) permite a los desarrolladores experimentar con determinadas características en desarrollo mediante una máquina en modo de desarrollador.
-   Hay cinco interfaces nuevas (consulte Jerarquía [de interfaces):](interface-hierarchy.md)
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Consulte información general sobre el modelo de sombreador [HLSL 6.0,](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md)que describe las operaciones intrínsecas de onda para sombreadores de cálculo y píxeles multiproceso.
-   El uso de [**ID3D12Device::SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) ha cambiado.
-   Algunas características nuevas de Direct3D 11 se describen en [Características de Direct3D 11.4.](../direct3d11/direct3d-11-4-features.md)
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) y [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) permiten el bloqueo en tiempo de **espera** para reducir la latencia pervieved.
-   [**ID3D12Device2::CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) y [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) habilitan las pruebas de **límites de profundidad** en hardware compatible.
-   [**ResolveSubresourceRegion permite**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) la **resolución parcial de** los subrecursos para ayudar a optimizar el rendimiento.
-   [**SetSamplePositions permite**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) **posiciones de ejemplo programables** en el hardware compatible.

## <a name="november-2016-documentation-update"></a>Actualización de documentación de noviembre de 2016

-   Revisión de los comentarios de [**ID3D12GraphicsCommandList::D iscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Aclaración de "Decadencia del estado a común" (consulte Uso de barreras de recursos para sincronizar estados de recursos [en Direct3D 12).](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)
-   El archivo de encabezado D3dx12.h, al que se hace referencia en Estructuras y funciones auxiliares para [D3D12,](helper-structures-and-functions-for-d3d12.md)se puede descargar directamente desde la biblioteca auxiliar [D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="august-2016-documentation-update-2"></a>Actualización 2 de la documentación de agosto de 2016

-   Una nueva sección de guía titulada Descripción de la capa de depuración [D3D12](understanding-the-d3d12-debug-layer.md).

    Se describen tres nuevas interfaces de capa de depuración (en modo de vista previa): [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Actualización 1 de la documentación de agosto de 2016

-   Revisión [del uso de barreras de recursos para sincronizar estados de recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Revisión del [acceso a recursos de varias colas.](./user-mode-heap-synchronization.md#multi-queue-resource-access)

## <a name="windows-10-version-1607"></a>Windows 10, versión 1607

Estos temas se han agregado a la documentación de Direct3D Windows 10, versión 1607.

-   [Root Signature Version 1.1](root-signature-version-1-1.md) : información general de las firmas raíz actualizadas, lo que permite a las aplicaciones especificar cómo son los descriptores y los datos estáticos o volátiles, lo que puede ayudar a optimizar el controlador de gráficos.
-   El [**método ID3D12Device1::CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) describe las ventajas de crear una biblioteca de canalizaciones.
-   Hay tres interfaces nuevas (consulte Jerarquía [de interfaces):](interface-hierarchy.md)
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Consulte información general sobre el modelo de sombreador [HLSL 6.0,](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md)que describe las operaciones intrínsecas de onda para sombreadores de cálculo y píxeles multiproceso.
-   El uso de [**ID3D12Device::SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) ha cambiado.
-   Algunas características nuevas de Direct3D 11 se describen en [Características de Direct3D 11.4.](../direct3d11/direct3d-11-4-features.md)
-   Se ha actualizado la gama de bibliotecas admitidas para Direct3D 12. Consulte la sección Herramientas y **bibliotecas admitidas** de Instalación del entorno de programación de [Direct3D 12.](directx-12-programming-environment-set-up.md)
-   [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md)
-   [Se muestra la frecuencia de actualización variable](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Mejoras de DXGI 1.5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)