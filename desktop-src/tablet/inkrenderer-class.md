---
description: Representa la administración de asignaciones desde la entrada de lápiz a la ventana de presentación. Use el objeto InkRenderer para mostrar la entrada de lápiz en una ventana. También puede usarlo para cambiar la posición y cambiar el tamaño del trazo.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Clase InkRenderer (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: f03b65a1ce009313b996fc7bede03f8c7425ff589fd29506c243f3161a851583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938725"
---
# <a name="inkrenderer-class"></a>InkRenderer (clase)

Representa la administración de asignaciones desde la entrada de lápiz a la ventana de presentación. Use el **objeto InkRenderer** para mostrar la entrada de lápiz en una ventana. También puede usarlo para cambiar la posición y cambiar el tamaño del trazo.

**InkRenderer** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

La **clase InkRenderer** define estas interfaces.



| Interfaz        | Descripción                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Este objeto implementa la interfaz COM **IInkRenderer.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkRenderer** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Dibuja trazos en un contexto de dispositivo.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Dibuja un trazo en el contexto de dispositivo de Windows especificado.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Recupera la transformación de objeto que se usó para representar la entrada de lápiz.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Recupera la transformación de vista que se usa para representar la entrada de lápiz.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Convierte una ubicación en coordenadas de espacio de entrada de lápiz para que esté en espacio en píxeles.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Convierte una matriz de puntos en coordenadas de espacio de entrada de lápiz en espacio en píxeles.<br/>                                                                          |
| [**Measure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcula el rectángulo en el contexto del dispositivo que contendrá una colección de trazos si se dibujaron con el **objeto InkRenderer.**<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcula el rectángulo en el contexto del dispositivo que contendrá un trazo si se dibujara con el **objeto InkRenderer.**<br/>                |
| [**Move**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Aplica una traducción a la transformación de vista en coordenadas de espacio de entrada de lápiz.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Convierte una ubicación en coordenadas de píxeles para que esté en el espacio de entrada de lápiz.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Convierte una matriz de puntos en coordenadas de espacio en píxeles en espacio de entrada de lápiz.<br/>                                                                          |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Aplica una rotación a la transformación de vista.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Escala la transformación de vista en las dimensiones X e Y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Establece la transformación de objetos que se usa para representar la entrada de lápiz.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Establece la transformación de vista que se usa para representar la entrada de lápiz.<br/>                                                                                           |



 

## <a name="remarks"></a>Comentarios

La impresión también se realiza a través del **objeto InkRenderer.**

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**InkDrawingAttributes (clase)**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

