---
title: Uso de Direct3D 11
description: En esta sección se muestra cómo usar la API de Microsoft Direct3D 11 para realizar varias tareas comunes.
ms.assetid: 9BDEDB68-3484-4683-85AF-B583971382C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bc4dad63c5fc12f2077481172061fc317135a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060835"
---
# <a name="how-to-use-direct3d-11"></a>Uso de Direct3D 11

En esta sección se muestra cómo usar la API de Microsoft Direct3D 11 para realizar varias tareas comunes.



| Tema                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo: Crear un dispositivo de referencia](overviews-direct3d-11-devices-create-ref.md)<br/>                                  | En este tema se muestra cómo crear un dispositivo de referencia que implementa una implementación de software altamente precisa del tiempo de ejecución.<br/>                                                                                                                                                    |
| [Cómo: Crear un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)<br/>                                      | En este tema se muestra cómo crear un dispositivo WARP que implementa un rasterizador de software de alta velocidad.<br/>                                                                                                                                                                                  |
| [Cómo: Crear una cadena de intercambio](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                 | En este tema se muestra cómo crear una cadena de intercambio que encapsula dos o más búferes que se usan para representar y mostrar. <br/>                                                                                                                                                      |
| [Cómo: Enumerar adaptadores](overviews-direct3d-11-devices-enum.md)<br/>                                               | En este tema se muestra cómo usar Microsoft Infraestructura de gráficos de DirectX (DXGI) para enumerar los adaptadores de gráficos disponibles en un equipo.<br/>                                                                                                                                        |
| [Cómo: Obtener modos de presentación del adaptador](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                            | En este tema se muestra cómo usar DXGI para obtener los modos de presentación válidos asociados a un adaptador.<br/>                                                                                                                                                                                     |
| [Cómo: Crear un dispositivo y un contexto inmediato](overviews-direct3d-11-devices-initialize.md)<br/>                      | En este tema se muestra cómo inicializar un [dispositivo](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                                                                                                        |
| [Cómo: Obtener el nivel de característica de dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/>                            | En este tema se muestra cómo obtener el nivel [de característica más alto](overviews-direct3d-11-devices-downlevel-intro.md) compatible con un [dispositivo](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                   |
| [Cómo: Crear un búfer de vértices](overviews-direct3d-11-resources-buffers-vertex-how-to.md)<br/>                        | En este tema se muestra cómo inicializar un búfer de [vértice estático,](overviews-direct3d-11-resources-buffers-intro.md)es decir, un búfer de vértices que no cambia.<br/>                                                                                                                  |
| [Cómo: Crear un búfer de índice](overviews-direct3d-11-resources-buffers-index-how-to.md)<br/>                         | En este tema se muestra cómo inicializar un búfer [de índice](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.<br/>                                                                                                                                           |
| [Cómo: Crear un búfer constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)<br/>                    | En este tema se muestra cómo inicializar un búfer [constante como](overviews-direct3d-11-resources-buffers-intro.md) preparación para la representación.<br/>                                                                                                                                         |
| [Cómo: Crear una textura](overviews-direct3d-11-resources-textures-create.md)<br/>                                    | En este tema se muestra cómo crear una textura.<br/>                                                                                                                                                                                                                                       |
| [Cómo: Inicializar una textura mediante programación](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)<br/> | En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas creadas con distintos tipos de usos.<br/>                                                                                                                                                             |
| [Cómo: Inicializar una textura a partir de un archivo](overviews-direct3d-11-resources-textures-how-to.md)<br/>                    | En este tema se muestra cómo usar Windows Imaging Component (WIC) para crear la textura y la vista por separado.<br/>                                                                                                                                                                      |
| [Cómo: Usar recursos dinámicos](how-to--use-dynamic-resources.md)<br/>                                                 | Puede crear y usar recursos dinámicos cuando la aplicación necesite cambiar los datos de esos recursos. Puede crear texturas y búferes para su uso dinámico.<br/>                                                                                                                              |
| [Cómo: Crear un sombreador de proceso](direct3d-11-advanced-stages-compute-create.md)<br/>                                  | En este tema se muestra cómo crear un sombreador de proceso.<br/>                                                                                                                                                                                                                                |
| [Cómo: Diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                 | En este tema se muestra cómo diseñar un sombreador de casco.<br/>                                                                                                                                                                                                                                  |
| [Cómo: Crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                 | En este tema se muestra cómo crear un sombreador de casco.<br/>                                                                                                                                                                                                                                   |
| [Cómo: Inicializar la fase del teselador](direct3d-11-advanced-stages-tessellator-initialize.md)<br/>                 | En este tema se muestra cómo inicializar la fase del teselador.<br/>                                                                                                                                                                                                                       |
| [Cómo: Diseñar un sombreador de dominio](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                             | En este tema se muestra cómo diseñar un sombreador de dominio.<br/>                                                                                                                                                                                                                                |
| [Cómo: Crear un sombreador de dominio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                             | En este tema se muestra cómo crear un sombreador de dominio.<br/>                                                                                                                                                                                                                                 |
| [Cómo: Compilar un sombreador](how-to--compile-a-shader.md)<br/>                                                           | En este tema se muestra cómo usar la [**función D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) en tiempo de ejecución para compilar el código del sombreador.<br/>                                                                                                                                          |
| [Cómo: Registrar una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md)<br/>                 | En este tema se muestra cómo crear y registrar una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                         |
| [Cómo: Reproducir una lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md)<br/>                | En este tema se muestra cómo reproducir una lista [de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                                 |
| [Comprobación de la compatibilidad con controladores](overviews-direct3d-11-render-multi-thread-support.md)<br/>                          | En este tema se muestra cómo determinar [](overviews-direct3d-11-render-multi-thread-intro.md) si las características de multithreading (incluida la creación de recursos y las listas de [comandos)](overviews-direct3d-11-render-multi-thread-command-list.md)se admiten para la aceleración de hardware.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de Direct3D 11](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

