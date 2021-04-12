---
description: Representa la administración de las asignaciones de entrada manuscrita a la ventana de presentación. Use el objeto InkRenderer para mostrar la entrada de lápiz en una ventana. También se puede usar para cambiar la posición y el tamaño del trazo.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Clase InkRenderer (Msinkaut. h)
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
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279383"
---
# <a name="inkrenderer-class"></a>Clase InkRenderer

Representa la administración de las asignaciones de entrada manuscrita a la ventana de presentación. Use el objeto **InkRenderer** para mostrar la entrada de lápiz en una ventana. También se puede usar para cambiar la posición y el tamaño del trazo.

**InkRenderer** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

La clase **InkRenderer** define estas interfaces.



| Interfaz        | Descripción                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Este objeto implementa la interfaz com **IInkRenderer** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkRenderer** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Dibuja trazos en un contexto de dispositivo.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Dibuja un trazo en el contexto de dispositivo de Windows especificado.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Recupera la transformación de objeto que se usó para representar la entrada de lápiz.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Recupera la transformación de vista que se usa para representar la entrada de lápiz.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Convierte una ubicación en coordenadas de espacio de tinta para que esté en el espacio en píxeles.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Convierte una matriz de puntos en las coordenadas del espacio de entrada en el espacio en píxeles.<br/>                                                                          |
| [**Medi**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcula el rectángulo en el contexto del dispositivo que contendría una colección de trazos si se dibujaron con el objeto **InkRenderer** .<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcula el rectángulo en el contexto del dispositivo que contendría un trazo si se dibujó con el objeto **InkRenderer** .<br/>                |
| [**Move**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Aplica una traslación a la transformación de la vista en coordenadas de espacio de tinta.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Convierte una ubicación en coordenadas de píxeles para que esté en el espacio de tinta.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Convierte una matriz de puntos en coordenadas de espacio en píxeles en el espacio de la entrada de lápiz.<br/>                                                                          |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Aplica un giro a la transformación de la vista.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Escala la transformación de la vista en la dimensión X e y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Establece la transformación de objeto que se usa para representar la entrada de lápiz.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Establece la transformación de la vista que se utiliza para representar la entrada de lápiz.<br/>                                                                                           |



 

## <a name="remarks"></a>Observaciones

La impresión también se realiza a través del objeto **InkRenderer** .

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Renderer (propiedad)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Clase InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

