---
description: 'Las marcas siguientes se usan para especificar opciones de representación de sprite para el parámetro flags en el método Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4dbf3e80e7cf6f7884d778860f9de61f5193f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997322"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Las marcas siguientes se usan para especificar opciones de representación de sprite para el parámetro flags en el [**método Begin:**](id3dxsprite--begin.md)



| \#Definir                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | El estado del dispositivo no se guardará ni restaurará cuando se llame a [**Begin**](id3dxsprite--begin.md) o [**End.**](id3dxsprite--end.md)                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | El estado de representación del dispositivo no se debe cambiar cuando [**se llama**](id3dxsprite--begin.md) a Begin. Se supone que el dispositivo está en un estado válido para dibujar vértices que contienen UsageIndex = 0 en los datos D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD y D3DDECLUSAGE \_ COLOR.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | Las transformaciones de mundo, vista y proyección no se modifican. Las transformaciones establecidas actualmente en el dispositivo se usan para transformar los sprites cuando se dibujan los sprites por lotes (cuando se llama a [**Flush**](id3dxsprite--flush.md) o [**End).**](id3dxsprite--end.md) Si no se especifica esta marca, se modifican las transformaciones de mundo, vista y proyección para que los sprites se dibujan en coordenadas de espacio en pantalla.              |
| D3DXSPRITEONES \_                | Cada sprite se girará sobre su centro para que esté orientado al visor. Se debe llamar primero a [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) o [**SetWorldViewRH.**](id3dxsprite--setworldviewrh.md)                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Habilita la combinación alfa con D3DRS \_ ALPHATESTENABLE establecido en **TRUE** (para alfa distinto de cero). D3DBLEND SRCALPHA será el estado de mezcla de origen \_ y D3DBLEND INVSRCALPHA será el estado de mezcla de destino en las llamadas a \_ [**SetRenderState.**](/windows/desktop/api) Vea [Alpha Blending State (Direct3D 9) (Estado de mezcla alfa [Direct3D 9]).](alpha-blending-state.md) [**ID3DXFont espera**](id3dxfont.md) que esta marca se establezca al dibujar texto. |
| TEXTURA DE ORDENACIÓN D3DXSPRITE \_ \_            | Ordene sprites por textura antes de dibujar. Esto puede mejorar el rendimiento al dibujar sprites no superpuestos de profundidad uniforme. También puede combinar D3DXSPRITE SORT TEXTURE con \_ \_ D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK o \_ D3DXSPRITE \_ SORT DEPTH \_ \_ BACKTOFRONT. Esto ordenará la lista de sprites por profundidad primero y segundo por textura.<br/>                                                                           |
| FRONTTOBACK DE PROFUNDIDAD \_ DE \_ ORDENACIÓN D3DXSPRITE \_ | Los sprites se ordenan por profundidad en orden de front-to-back antes del dibujo. Este procedimiento se recomienda al dibujar sprites opacos de diferentes profundidades. Puede combinar D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK con \_ D3DXSPRITE SORT TEXTURE para ordenar primero por profundidad \_ y segundo por \_ textura.<br/>                                                                                                                                   |
| D3DXSPRITE \_ SORT \_ DEPTH \_ BACKTOFRONT | Los sprites se ordenan por profundidad en orden de back-to-front antes de dibujar. Este procedimiento se recomienda al dibujar sprites transparentes de distintas profundidades. Puede combinar D3DXSPRITE \_ SORT \_ DEPTH BACKTOFRONT con \_ D3DXSPRITE SORT TEXTURE para ordenar primero por profundidad \_ y segundo por \_ textura.<br/>                                                                                                                              |
| D3DXSPRITE \_ NO \_ \_ ADDREF \_ TEXTURE | Deshabilita la llamada a AddRef() en cada dibujo y Release() en Flush() para mejorar el rendimiento.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3dx9core.h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




