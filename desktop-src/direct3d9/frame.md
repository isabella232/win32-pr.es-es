---
description: Define un marco de coordenadas o &\# 0034;marco de reference.&\# 0034; La plantilla Marco está abierta y puede contener cualquier objeto. Las funciones de carga de malla D3DX reconocen las instancias de plantilla Mesh, FrameTransformMatrix y Frame como objetos secundarios al cargar una instancia de Frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Marco (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523038"
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

 

 



