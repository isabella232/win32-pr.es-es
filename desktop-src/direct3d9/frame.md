---
description: Define un marco de coordenadas o &\# 0034;marco de reference.&\# 0034; La plantilla Marco está abierta y puede contener cualquier objeto. Las funciones de carga de malla D3DX reconocen las instancias de plantilla Mesh, FrameTransformMatrix y Frame como objetos secundarios al cargar una instancia de Frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Marco (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060646"
---
# <a name="frame-direct3d-9-graphics"></a>Marco (gráficos de Direct3D 9)

Define un marco de coordenadas o "marco de referencia". La plantilla Marco está abierta y puede contener cualquier objeto. Las funciones de carga de malla D3DX reconocen las instancias de plantilla [**Mesh,**](mesh.md) [**FrameTransformMatrix**](frametransformmatrix.md)y **Frame** como objetos secundarios al cargar una **instancia de Frame.**

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

La plantilla de marco reconoce los nodos **secundarios Frame** y [**Mesh**](mesh.md) dentro de un marco y puede reconocer plantillas definidas por el usuario a través de una función de devolución de llamada.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



