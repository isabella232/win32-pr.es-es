---
description: 'En este tema se proporcionan dos vistas de alto nivel de la arquitectura de Direct3D:'
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Arquitectura de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e557b7a36aadcaa8b96899047a721741ecef2156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152329"
---
# <a name="direct3d-architecture-direct3d-9"></a>Arquitectura de Direct3D (Direct3D 9)

En este tema se proporcionan dos vistas de alto nivel de la arquitectura de Direct3D:

-   [Canalización de gráficos de Direct3D](#direct3d-graphics-pipeline) : una vista de la arquitectura de procesamiento interno del sistema de representación de Direct3D.
-   [Integración del sistema de Direct3D](#direct3d-system-integration) : una vista de cómo Direct3D media entre una aplicación y el hardware de gráficos.

## <a name="direct3d-graphics-pipeline"></a>Canalización de gráficos Direct3D

La canalización de gráficos proporciona la potencia para procesar y representar de forma eficaz las escenas de Direct3D en una pantalla, aprovechando el hardware disponible. En el diagrama siguiente se muestran los bloques de creación de la canalización:

![diagrama de la canalización de gráficos Direct3D](images/blockdiag-graphics.png)



| Componente de canalización  | Descripción                                                                                                                                                                                      | Temas relacionados                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Datos de vértices         | Los vértices de modelo sin transformar se almacenan en búferes de memoria de vértices.                                                                                                                                | [Búferes de vértices (Direct3D 9)](vertex-buffers.md), [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Datos primitivos      | Se hace referencia a las primitivas geométricas, incluidos los puntos, líneas, triángulos y polígonos, en los datos de vértice con búferes de índice.                                                                    | [Búferes de índice (Direct3D 9)](index-buffers.md), [**IDirect3DIndexBuffer9**](/windows/desktop/api), [primitivos](primitives.md), [primitivos de orden superior (Direct3D 9)](higher-order-primitives.md) |
| Teselación        | La unidad tesselator convierte los primitivos de orden superior, los mapas de desplazamiento y las revisiones de malla en ubicaciones de vértices y almacena dichas ubicaciones en búferes de vértices.                                      | [Teselación (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Procesamiento de vértices   | Las transformaciones de Direct3D se aplican a los vértices almacenados en el búfer de vértices.                                                                                                                    | [Canalización de vértices (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Procesamiento de geometría | El recorte, la selección de la cara posterior, la evaluación de atributos y la rasterización se aplican a los vértices transformados.                                                                                    | [Canalización de píxeles (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Superficie con textura    | Las coordenadas de textura para las superficies de Direct3D se proporcionan a Direct3D a través de la interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .                                                         | [Texturas de Direct3D (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Muestra de textura     | El filtrado de nivel de detalle de textura se aplica a los valores de textura de entrada.                                                                                                                            | [Texturas de Direct3D (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Procesamiento de píxeles    | Las operaciones del sombreador de píxeles usan datos de geometría para modificar los datos de textura y vértices de entrada, produciendo valores de color de píxeles de salida.                                                                           | [Canalización de píxeles (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Representación de píxeles     | Los procesos de representación finales modifican los valores de color de los píxeles con las pruebas alfa, de profundidad o de estarcido, o aplicando la mezcla o niebla alfa. Todos los valores de píxel resultantes se muestran en la pantalla de salida. | [Canalización de píxeles (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Integración del sistema Direct3D

En el diagrama siguiente se muestran las relaciones entre una aplicación de ventana, Direct3D, GDI y el hardware:

![diagrama de la relación entre Direct3D y otros componentes del sistema](images/d3dsysint.png)

Direct3D expone una interfaz independiente del dispositivo a una aplicación. Las aplicaciones de Direct3D pueden existir junto con las aplicaciones GDI y ambos tienen acceso al hardware gráfico del equipo a través del controlador de dispositivo de la tarjeta gráfica. A diferencia de GDI, Direct3D puede aprovechar las características de hardware mediante la creación de un dispositivo Hal.

Un dispositivo Hal proporciona aceleración de hardware a las funciones de canalización de gráficos, en función del conjunto de características admitido por la tarjeta gráfica. Los métodos de Direct3D se proporcionan para recuperar funcionalidades de visualización de dispositivos en tiempo de ejecución. (Vea [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)). Si el hardware no proporciona una funcionalidad, la HAL no la notifica como una capacidad de hardware.

Para obtener más información sobre los dispositivos de referencia y Hal compatibles con Direct3D, consulte [tipos de dispositivo (Direct3D 9)](device-types.md).

## <a name="related-topics"></a>Temas relacionados

[Introducción](getting-started.md)
