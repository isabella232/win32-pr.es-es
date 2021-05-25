---
description: Marcas de funcionalidad del controlador D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343210"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Marcas de funcionalidad del controlador D3DDEVCAPS2.



| \#Definir                                        | Descripción                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | El dispositivo admite la teselación adaptable de revisiones RT                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | El dispositivo admite la teselación adaptable de N revisiones.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ PUEDE \_ EXTENDERSE DESDE \_ \_ TEXTURAS   | El dispositivo [**admite StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mediante una textura como origen.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | El dispositivo admite mapas de desplazamiento para N revisiones.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | El dispositivo admite mapas de desplazamiento previamente muestreados para N revisiones. Para obtener más información sobre la asignación de desplazamiento, vea [Asignación de desplazamiento (Direct3D 9).](displacement-mapping.md)                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | El dispositivo admite desplazamientos de flujo.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Varios elementos de vértice pueden compartir el mismo desplazamiento en una secuencia si el dispositivo establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET y la declaración de vértice no tiene un elemento con \_ D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
