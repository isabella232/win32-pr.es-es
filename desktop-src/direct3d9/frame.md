---
description: Define un marco de coordenadas o &\# 0034; marco de referencia. &\# 0034; La plantilla de marco está abierta y puede contener cualquier objeto. Las funciones de carga de malla de D3DX reconocen las instancias de la plantilla de fotogramas, FrameTransformMatrix y malla como objetos secundarios al cargar una instancia de Frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Fotograma (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906442"
---
# <a name="frame-direct3d-9-graphics"></a>Fotograma (gráficos de Direct3D 9)

Define un marco de coordenadas o "marco de referencia". La plantilla de marco está abierta y puede contener cualquier objeto. Las funciones de carga de malla de D3DX reconocen las instancias de la plantilla de **fotogramas** , [**FrameTransformMatrix**](frametransformmatrix.md)y [**malla**](mesh.md)como objetos secundarios al cargar una instancia de **Frame** .

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

La plantilla de marco reconoce los nodos de **fotogramas** y [**malla**](mesh.md) secundarios dentro de un marco y puede reconocer las plantillas definidas por el usuario a través de una función de devolución de llamada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



