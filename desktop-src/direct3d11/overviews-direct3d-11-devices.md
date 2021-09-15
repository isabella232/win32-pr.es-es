---
title: Dispositivos (gráficos de Direct3D 11)
description: En esta sección se describen los objetos device y device-context de Direct3D 11.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dda010b3801952e90514fac6307556f8f6fbaff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566680"
---
# <a name="devices-direct3d-11-graphics"></a>Dispositivos (gráficos de Direct3D 11)

Un dispositivo Direct3D asigna y destruye objetos, representa primitivos y se comunica con un controlador de gráficos y el hardware. En Direct3D 11, un dispositivo se separa en un objeto de dispositivo para crear recursos y un objeto de contexto de dispositivo, que realiza la representación. En esta sección se describen los objetos device y device-context de Direct3D 11.

Los objetos creados a partir de un dispositivo no se pueden usar directamente con otros dispositivos. Use un recurso compartido para compartir datos entre varios dispositivos, con la restricción de que un objeto compartido solo lo pueda usar el dispositivo que lo creó.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                                         | Descripción                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a un dispositivo en Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o varios contextos. esta separación está diseñada para facilitar el multithreading.<br/>                                                  |
| [Capas de software](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | El entorno de ejecución de Direct3D 11 se construye con capas, empezando por la funcionalidad básica en el núcleo y creando funcionalidades opcionales y de ayuda para el desarrollador en capas externas. En esta sección se describe la funcionalidad de cada capa.<br/> |
| [Limitaciones al crear dispositivos DE REFERENCIA y WARP](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Existen algunas limitaciones para crear dispositivos WARP y Reference en Direct3D 10.1 y Direct3D 11.0. En este tema se de abordan esas limitaciones.<br/>                                                                                              |
| [Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | En esta sección se describe cómo Direct3D 11 está diseñado para admitir hardware nuevo y existente, de DirectX 9 a DirectX 11.<br/>                                                                                                             |
| [Uso de datos de características de Direct3D 11 para complementar los niveles de características de Direct3D](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Descubra cómo comprobar la compatibilidad del dispositivo con características opcionales, incluidas las características que se agregaron en versiones recientes de Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Temas sobre dispositivos



| Tema                                                                                                                                                                                                                                                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Cómo: Crear un dispositivo de referencia](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Describe cómo crear un dispositivo de referencia.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Cómo: Crear un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Describe cómo crear un dispositivo WARP.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Cómo: Crear una cadena de intercambio](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Describe cómo crear una cadena de intercambio.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Cómo: Enumerar adaptadores](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Describe cómo enumerar los adaptadores de pantalla físicos.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Cómo: Obtener modos de presentación del adaptador](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Describe cómo obtener las funcionalidades de visualización admitidas de un adaptador.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Cómo: Crear un dispositivo y un contexto inmediato](overviews-direct3d-11-devices-initialize.md)<br/> | Describe cómo inicializar un dispositivo.<br/>                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

 





