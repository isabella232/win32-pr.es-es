---
description: Constantes de generación de mapas normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3a3d2f35fa409e4432dd7600cb544df25110d10aa9af7f5ee18fd622ea1309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374955"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Constantes de generación de mapas normales.



| \#Definir                            | Descripción                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica que los píxeles del borde de la textura en el eje u deben reflejarse, no ajustarse.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica que los píxeles del borde de la textura del eje v deben reflejarse, no ajustarse.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | Igual que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Invierte la dirección de cada normal.                                                                                                                                                              |
| \_OCLUSIÓN DE PROCESO DE D3DX NORMALMAP \_ \_ | Calcula el término de oclusión por píxel y lo codifica en el alfa. Un alfa de 1 significa que el píxel no se oculta de ninguna manera, y un alfa de 0 significa que el píxel está completamente oculto. |



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3dx9tex.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



