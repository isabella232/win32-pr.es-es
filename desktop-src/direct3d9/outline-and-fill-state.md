---
description: Las primitivas que no tienen texturas se representan con el color especificado por su material, o con los colores especificados para los vértices, si los hay.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Esquema y estado de relleno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966575"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Esquema y estado de relleno (Direct3D 9)

Las primitivas que no tienen texturas se representan con el color especificado por su material, o con los colores especificados para los vértices, si los hay. Puede seleccionar el método para rellenarlos especificando un valor definido por el tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) para el estado de representación FILLMODE de D3DRS. \_

Para habilitar la dithering, la aplicación debe pasar el valor enumerado D3DRS DITHERENABLE como primer parámetro \_ a [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). Debe establecer el segundo parámetro en **TRUE para** habilitar la dithering y **FALSE** para deshabilitarlo.

En ocasiones, dibujar el último píxel de una línea puede provocar una superposición antiestética con las primitivas circundantes. Puede controlar esto mediante el valor enumerado D3DRS \_ LASTPIXEL. Sin embargo, no modifique esta configuración sin que se le realice ninguna instrucción forethought. En algunas condiciones, la supresión de la representación del último píxel puede provocar lagunas antiestéticas entre las primitivas.

Los contornos de objeto se pueden dibujar estableciendo el patrón de dibujo de línea adecuado. El estado de dibujo de línea predeterminado es dibujar líneas sólidas. Para obtener más información, vea Compatibilidad con el dibujo de líneas en el estado de representación [D3DX (Direct3D 9).](line-drawing-support-in-d3dx.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
