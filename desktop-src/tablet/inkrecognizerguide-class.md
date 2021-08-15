---
description: Representa el área que usa el reconocedor en el que se puede dibujar la entrada manuscrita. El área se conoce como guía de reconocimiento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Clase InkRecognizerGuide (Msguideut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 758c2ac58803b0086a4a4083545a66d250799b414bd44e3814c90de37ca9d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675679"
---
# <a name="inkrecognizerguide-class"></a>InkRecognizerGuide (clase)

Representa el área que usa el reconocedor en el que se puede dibujar la entrada manuscrita. El área se conoce como guía de reconocimiento.

**InkRecognizerGuide** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La **clase InkRecognizerGuide** define estas interfaces.



| Interfaz               | Descripción                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Este objeto implementa la interfaz **COM IInkRecognizerGuide.**<br/> |



 

### <a name="properties"></a>Propiedades

La **clase InkRecognizerGuide** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Columnas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lectura/escritura<br/> | Obtiene o establece el número de columnas del cuadro de guía.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lectura/escritura<br/> | Obtiene o establece el cuadro que se dibuja físicamente en la pantalla de la tableta y en el que tiene lugar la escritura.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lectura/escritura<br/> | Obtiene o establece datos de guía para desarrolladores de C++.<br/>                                                                         |
| [**Midline**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lectura/escritura<br/> | Obtiene o establece el alto de línea media. La altura de la línea media es la distancia desde la línea base hasta la línea media del cuadro dibujado.<br/> |
| [**Filas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lectura/escritura<br/> | Obtiene o establece el número de filas del cuadro de guía.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lectura/escritura<br/> | Obtiene o establece el área de escritura invisible del cuadro de guía en el que la escritura puede tener lugar realmente.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

De forma predeterminada, no hay ninguna guía de reconocedor. Una guía predeterminada tiene todos los valores de propiedad establecidos en 0. Debe usar las propiedades de este objeto para establecer la guía.

Si la aplicación ha dibujado directrices en la pantalla en la que se espera que el usuario escriba, la aplicación debe establecer los valores de las propiedades de la guía del reconocedor para informar al reconocedor. Estas propiedades son solo para uso del reconocedor. Establecerlos no dibuja, por sí solo, pistas visuales en la pantalla. La aplicación o el control dibujan las pistas visuales.

La guía del reconocedor puede constar de filas y columnas, y estas dan al reconocedor un contexto mejor en el que realizar el reconocimiento. Las letras como "t" e "I" se reconocen más fácilmente cuando se usa una guía para dar contexto a la entrada de lápiz. Por ejemplo, puede dibujar líneas horizontales en una pantalla que muestren dónde debe producirse la escritura (este tipo de guía constaría solo de filas y ninguna columna). Al escribir en las líneas, en lugar de algún espacio arbitrario, mejora la precisión del reconocimiento.

La guía especifica los límites de la entrada de lápiz en coordenadas de espacio de entrada de lápiz.

La [**propiedad DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) puede definir un cuadro que tiene el mismo tamaño que o menor que el cuadro definido por la [**propiedad WritingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)

En la ilustración siguiente se muestran los elementos de una guía de reconocedor con dos filas y sin columnas.

![ilustración en la que se muestran los elementos de la guía del reconocedor](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Además de dibujar líneas en la pantalla que muestran a los usuarios dónde escribir, puede dibujar celdas en la pantalla en las que se escriben caracteres o palabras. Esto se denomina entrada boxeada y es útil con algunos idiomas asiáticos. Para determinar si el reconocedor es capaz de realizar una entrada boxing, llame a la [**propiedad Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del [**objeto IInkRecognizer.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)

En la ilustración siguiente se muestra una guía de reconocedor con cuatro columnas.

![ilustración en la que se muestra la guía del reconocedor con cuatro columnas](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkRecognizer (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
</dt> </dl>

 

