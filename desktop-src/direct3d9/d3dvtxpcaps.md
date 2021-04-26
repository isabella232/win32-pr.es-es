---
description: Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998662"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.



| \#Definir                                | Descripción                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | El dispositivo puede hacer luces direccionales.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | El dispositivo puede hacer visor local.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Cuando se establece este límite, el dispositivo admite los estados de material de color: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ NO TIENE UN \_ \_ NOLOCALVIEWER DE TEXGEN | El dispositivo no admite la generación de texturas en modo de visor no local.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | El dispositivo puede hacer luces posicionales (incluye un punto y un punto).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | El dispositivo puede realizar la hazjagen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | El dispositivo admite D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| INTERPOLACIÓN DE D3DVTXPCAPS \_                   | El dispositivo puede realizar la interpolación de vértices.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



