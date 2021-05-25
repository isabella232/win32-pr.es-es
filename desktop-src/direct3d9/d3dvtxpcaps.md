---
description: Obtenga información sobre una combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad3b5eca7a264e489382d80b336f5b2c660e1a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342920"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.



| \#Definir                                | Descripción                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | El dispositivo puede hacer luces direccionales.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | El dispositivo puede hacer visor local.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Cuando se establece este límite, el dispositivo admite los estados de material de color: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ NO HAY NINGÚN \_ \_ NOLOCALVIEWER DE TEXASGEN | El dispositivo no admite la generación de texturas en el modo de visor no local.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | El dispositivo puede realizar luces posicionales (incluye un punto y un punto).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | El dispositivo puede realizar la hazgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | El dispositivo admite D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| INTERPOLACIÓN DE D3DVTXPCAPS \_                   | El dispositivo puede realizar la interpolación de vértices.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



