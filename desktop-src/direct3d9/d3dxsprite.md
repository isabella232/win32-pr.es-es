---
description: 'Las marcas siguientes se usan para especificar las opciones de representación de Sprite en el parámetro flags en el método Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c394d2606584ec5f56aa28661a2da286f000a66d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536436"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Las marcas siguientes se usan para especificar las opciones de representación de Sprite en el parámetro flags en el método [**Begin**](id3dxsprite--begin.md) :



|                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
| D3DXSPRITE \_ DONOTSAVESTATE           | El estado del dispositivo no se guardará ni restaurará cuando se llame a [**Begin**](id3dxsprite--begin.md) o [**End**](id3dxsprite--end.md) .                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | El estado de representación del dispositivo no se debe cambiar cuando se llama a [**Begin**](id3dxsprite--begin.md) . Se supone que el dispositivo está en un estado válido para dibujar vértices que contienen UsageIndex = 0 en los \_ datos de color D3DDECLUSAGE Position, D3DDECLUSAGE \_ TEXCOORD y D3DDECLUSAGE \_ .                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | Las transformaciones mundo, vista y proyección no se modifican. Las transformaciones establecidas actualmente en el dispositivo se utilizan para transformar los sprites cuando se dibujan los sprites por lotes (cuando se llama a [**Flush**](id3dxsprite--flush.md) o [**End**](id3dxsprite--end.md) ). Si no se especifica esta marca, se modifican las transformaciones mundo, vista y proyección para que los sprites se dibujen en coordenadas de espacio de pantalla.              |
| D3DXSPRITE de la \_ cartelera                | Cada Sprite se girará alrededor de su centro para que se enfrente al visor. Se debe llamar primero a [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) o [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) .                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Habilita la combinación alfa con D3DRS \_ ALPHATESTENABLE establecido en **true** (para alfa distinto de cero). D3DBLEND \_ SRCALPHA será el estado de Blend de origen y D3DBLEND \_ INVSRCALPHA será el estado de mezcla de destino en las llamadas a [**SetRenderState**](/windows/desktop/api). Vea [Estado de mezcla alfa (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) espera que esta marca se establezca al dibujar texto. |
| D3DXSPRITE \_ ordenar \_ textura            | Ordene los sprites por textura antes del dibujo. Esto puede mejorar el rendimiento al dibujar sprites no superpuestos de profundidad uniforme. También puede combinar la \_ textura de ordenación D3DXSPRITE \_ con la profundidad de ordenación D3DXSPRITE \_ \_ \_ FRONTTOBACK o la profundidad de \_ ordenación D3DXSPRITE \_ \_ BACKTOFRONT. Esto ordenará la lista de sprites por profundidad y por segundo.<br/>                                                                           |
| D3DXSPRITE \_ profundidad de ordenación \_ \_ FRONTTOBACK | Los sprites se ordenan por profundidad en orden ascendente antes del dibujo. Se recomienda este procedimiento al dibujar sprites opacos de distintas profundidades. Puede combinar la \_ profundidad de ordenación D3DXSPRITE \_ \_ FRONTTOBACK con D3DXSPRITE \_ ordenar \_ textura para ordenar primero por profundidad y segundo por textura.<br/>                                                                                                                                   |
| D3DXSPRITE \_ profundidad de ordenación \_ \_ BACKTOFRONT | Los sprites se ordenan por profundidad en orden ascendente antes del dibujo. Se recomienda este procedimiento al dibujar sprites transparentes de distintas profundidades. Puede combinar la \_ profundidad de ordenación D3DXSPRITE \_ \_ BACKTOFRONT con D3DXSPRITE \_ ordenar \_ textura para ordenar primero por profundidad y segundo por textura.<br/>                                                                                                                              |
| \_Textura D3DXSPRITE \_ no \_ ADDREF \_ | Deshabilita la llamada a AddRef () en cada Draw y Release () en Flush () para mejorar el rendimiento.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3dx9core. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




