---
description: Los primitivos que no tienen texturas se representan con el color especificado por su material o con los colores especificados para los vértices, si los hay.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Esquema y estado de relleno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714673"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Esquema y estado de relleno (Direct3D 9)

Los primitivos que no tienen texturas se representan con el color especificado por su material o con los colores especificados para los vértices, si los hay. Puede seleccionar el método para rellenarlos especificando un valor definido por el tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) para el estado de \_ representación de D3DRS FILLMODE.

Para habilitar el tramado, la aplicación debe pasar el \_ valor enumerado de D3DRS DITHERENABLE como primer parámetro a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). Debe establecer el segundo parámetro en **true** para habilitar el tramado y **false** para deshabilitarlo.

En ocasiones, dibujar el último píxel en una línea puede provocar una superposición de forma no valiosa con los primitivos circundantes. Puede controlar esto mediante el \_ valor enumerado de D3DRS LASTPIXEL. Sin embargo, no modifique este valor sin ningún preprevisión. En algunas condiciones, suprimir la representación del último píxel puede producir brechas de percepción entre primitivas.

Los contornos de objeto se pueden dibujar estableciendo el patrón de dibujo de línea adecuado. El estado de dibujo de línea predeterminado es dibujar líneas sólidas. Para obtener más información, consulte [compatibilidad con el dibujo de líneas en el estado de representación de D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
