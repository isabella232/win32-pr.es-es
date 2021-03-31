---
description: Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423475"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                                | Descripción                                                                                                                                                                                        |
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | El dispositivo puede realizar luces direccionales.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | El dispositivo puede realizar el visor local.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Cuando se establece este límite, el dispositivo admite los Estados de material de color: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ \_ TEXGEN \_ NONLOCALVIEWER | El dispositivo no admite la generación de texturas en modo de visor no local.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | El dispositivo puede realizar luces posicionales (incluye punto y lugar).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | El dispositivo puede hacer texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | El dispositivo es compatible con D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| Intercalación de D3DVTXPCAPS \_                   | El dispositivo puede realizar la interpolación de vértices.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



