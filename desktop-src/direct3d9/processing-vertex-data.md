---
description: La interfaz IDirect3DDevice9 admite el procesamiento de vértices tanto en software como en hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Procesamiento de datos de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4656aadee8f39c61be438f85ae0829f0b10dac42c7e5c9014b6ba8c164b3257b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118615"
---
# <a name="processing-vertex-data-direct3d-9"></a>Procesamiento de datos de vértices (Direct3D 9)

La [**interfaz IDirect3DDevice9 admite el**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) procesamiento de vértices tanto en software como en hardware. En general, las funcionalidades del dispositivo para el procesamiento de vértices de hardware y software no son idénticas. Las funcionalidades de hardware son variables, según el adaptador de pantalla y el controlador, mientras que las funcionalidades de software son fijas.

Las marcas siguientes controlan el comportamiento del procesamiento de vértices para la capa de abstracción de hardware (HIB) y los dispositivos de referencia.

-   D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING
-   D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING
-   D3DCREATE \_ MIXED \_ VERTEXPROCESSING

Especifique una de las marcas de comportamiento de procesamiento de vértices al llamar a [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). La marca de modo mixto permite que el dispositivo realice el procesamiento de vértices de software y hardware. Solo se puede establecer una marca de procesamiento de vértices para un dispositivo en cualquier momento. Tenga en cuenta que la marca D3DCREATE HARDWARE VERTEXPROCESSING debe establecerse al crear un dispositivo puro \_ \_ (D3DCREATE \_ PUREDEVICE).

Para evitar las funcionalidades de procesamiento de vértices duales en un único dispositivo, solo se pueden consultar las funcionalidades de procesamiento de vértices de hardware en tiempo de ejecución. Las funcionalidades de procesamiento de vértices de software son fijas y no se pueden consultar en tiempo de ejecución.

El miembro VertexProcessingCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina las funcionalidades de procesamiento de vértices de hardware del dispositivo.

Para el procesamiento de vértices de software, se admiten las siguientes funcionalidades.

-   Miembro D3DVTXPCAPS \_ DIRECTIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   El miembro LOCALVIEWER D3DVTXPCAPS \_ [de D3DVTXPCAPS](d3dvtxpcaps.md)
-   Miembro D3DVTXPCAPS \_ MATERIALSOURCE7 de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   El miembro D3DVTXPCAPS \_ POSITIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   El miembro D3DVTXPCAPS \_ DE TEXGEN [de D3DVTXPCAPS](d3dvtxpcaps.md)
-   El miembro D3DVTXPCAPS \_ TWEENING de [D3DVTXPCAPS](d3dvtxpcaps.md)

Además, en la tabla siguiente se enumeran los valores que se establecen para los miembros de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para un dispositivo en modo de procesamiento de vértices de software.



| Miembro                 | Funcionalidades de procesamiento de vértices de software |
|------------------------|-----------------------------------------|
| MaxActiveLights        | ilimitadas                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

En general, cualquier aplicación que esté enlazada al procesamiento de vértices debe usar un dispositivo DE LAI. El procesamiento de vértices de software proporciona un conjunto garantizado de funcionalidades de procesamiento de vértices, incluido un número ilimitado de luces y compatibilidad completa con sombreadores de vértices programables. Puede alternar entre el procesamiento de vértices de hardware y software en cualquier momento cuando se usa el dispositivo DEI (que es el único tipo de dispositivo que admite el procesamiento de vértices de hardware y software). El único requisito es que los búferes de vértices utilizados para el procesamiento de vértices de software se deban asignar en la memoria del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
