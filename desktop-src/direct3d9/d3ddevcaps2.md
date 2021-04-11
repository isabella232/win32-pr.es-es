---
description: Marcas de capacidad del controlador D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274938"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Marcas de capacidad del controlador D3DDEVCAPS2.



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                                        | Descripción                                                                                                                                                                                                               |
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | El dispositivo admite teselación adaptable de RT-patchs                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | El dispositivo admite teselación adaptable de N-patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ puede \_ STRETCHRECT \_ de \_ texturas   | El dispositivo admite [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) con una textura como origen.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | El dispositivo admite los mapas de desplazamiento para N-patches.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | El dispositivo admite los mapas de desplazamiento premuestreados para N-patches. Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md).                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | El dispositivo admite desplazamientos de flujo.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Varios elementos VERTEX pueden compartir el mismo desplazamiento en un flujo si \_ el dispositivo establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET y la declaración de vértices no tiene un elemento con D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
