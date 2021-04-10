---
description: La interfaz IDirect3DDevice9 admite el procesamiento de vértices en software y hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Procesar datos de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906753"
---
# <a name="processing-vertex-data-direct3d-9"></a>Procesar datos de vértices (Direct3D 9)

La interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) admite el procesamiento de vértices en software y hardware. En general, las capacidades del dispositivo para el procesamiento de vértices de software y hardware no son idénticas. Las capacidades de hardware son variables, dependiendo del adaptador de pantalla y del controlador, mientras que las capacidades de software son fijas.

Las marcas siguientes controlan el comportamiento del procesamiento de vértices para la capa de abstracción de hardware (HAL) y los dispositivos de referencia.

-   D3DCREATE \_ software \_ VERTEXPROCESSING
-   \_VERTEXPROCESSING de hardware D3DCREATE \_
-   D3DCREATE \_ Mixed \_ VERTEXPROCESSING

Especifique una de las marcas de comportamiento de procesamiento de vértices al llamar a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). La marca de modo mixto permite que el dispositivo realice el procesamiento de vértices de software y hardware. Solo se puede establecer una marca de procesamiento de vértices para un dispositivo en un momento dado. Tenga en cuenta que \_ se debe establecer la marca D3DCREATE de hardware \_ VERTEXPROCESSING al crear un dispositivo puro (D3DCREATE \_ PUREDEVICE).

Para evitar las capacidades de procesamiento de vértices duales en un único dispositivo, solo se pueden consultar en tiempo de ejecución las capacidades de procesamiento de vértices de hardware. Las capacidades de procesamiento de vértices de software son fijas y no se pueden consultar en tiempo de ejecución.

El miembro VertexProcessingCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina las capacidades de procesamiento de vértices de hardware del dispositivo.

Para el procesamiento de vértices de software, se admiten las siguientes funcionalidades.

-   el \_ miembro D3DVTXPCAPS DIRECTIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   el \_ miembro D3DVTXPCAPS LOCALVIEWER de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   el \_ miembro D3DVTXPCAPS MATERIALSOURCE7 de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   el \_ miembro D3DVTXPCAPS POSITIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   el \_ miembro D3DVTXPCAPS TEXGEN de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   \_miembro de intercalación D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)

Además, en la tabla siguiente se enumeran los valores que se establecen para los miembros de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para un dispositivo en el modo de procesamiento de vértices de software.



| Miembro                 | Capacidades de procesamiento de vértices de software |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Sin límite                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

En general, cualquier aplicación enlazada al procesamiento de vértices debe usar un dispositivo HAL. El procesamiento de vértices de software proporciona un conjunto garantizado de funcionalidades de procesamiento de vértices, incluido un número ilimitado de luces y compatibilidad total con los sombreadores de vértices programables. Puede alternar entre el procesamiento de vértices de software y hardware en cualquier momento cuando se usa el dispositivo HAL (que es el único tipo de dispositivo que admite el procesamiento de vértices de hardware y software). El único requisito es que los búferes de vértices usados para el procesamiento de vértices de software deben asignarse en la memoria del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
