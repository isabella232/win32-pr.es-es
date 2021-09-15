---
description: Constantes de generación de mapas normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575264"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Constantes de generación de mapas normales.



| \#Definir                            | Descripción                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica que los píxeles del borde de la textura en el eje u deben reflejarse, no ajustarse.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica que los píxeles del borde de la textura del eje v deben reflejarse, no ajustarse.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | Igual que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Invierte la dirección de cada normal.                                                                                                                                                              |
| OCLUSIÓN \_ DE PROCESO DE D3DX NORMALMAP \_ \_ | Calcula el término de oclusión por píxel y lo codifica en el alfa. Un alfa de 1 significa que el píxel no se oculta de ninguna manera, y un alfa de 0 significa que el píxel está completamente oculto. |



 

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

 

 



