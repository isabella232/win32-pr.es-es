---
description: Representa el área que utiliza el reconocedor en el que se puede dibujar la entrada manuscrita. El área se conoce como la guía de reconocimiento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Clase InkRecognizerGuide (Msinkaut. h)
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
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279384"
---
# <a name="inkrecognizerguide-class"></a>Clase InkRecognizerGuide

Representa el área que utiliza el reconocedor en el que se puede dibujar la entrada manuscrita. El área se conoce como la guía de reconocimiento.

**InkRecognizerGuide** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La clase **InkRecognizerGuide** define estas interfaces.



| Interfaz               | Descripción                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Este objeto implementa la interfaz com **IInkRecognizerGuide** .<br/> |



 

### <a name="properties"></a>Propiedades

La clase **InkRecognizerGuide** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Columnas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lectura/escritura<br/> | Obtiene o establece el número de columnas del cuadro guía.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lectura/escritura<br/> | Obtiene o establece el cuadro que se dibuja físicamente en la pantalla de la tableta y en el que tiene lugar la escritura.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lectura/escritura<br/> | Obtiene o establece los datos de la guía para los desarrolladores de C++.<br/>                                                                         |
| [**Elips**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lectura/escritura<br/> | Obtiene o establece el alto de la media media. El alto de línea media es la distancia desde la línea base hasta la línea media del cuadro dibujado.<br/> |
| [**Las**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lectura/escritura<br/> | Obtiene o establece el número de filas del cuadro guía.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lectura/escritura<br/> | Obtiene o establece el área de escritura invisible del cuadro de guía en el que se puede producir realmente la escritura.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

De forma predeterminada, no hay ninguna guía de reconocimiento. Una guía predeterminada tiene todos los valores de propiedad establecidos en 0. Debe utilizar las propiedades de este objeto para establecer la guía.

Si la aplicación ha dibujado instrucciones en la pantalla en la que se espera que el usuario escriba, la aplicación debe establecer los valores de las propiedades de la guía del reconocedor para informar al reconocedor. Estas propiedades son solo para el uso del reconocedor. El establecimiento de ellos no dibuja pistas visuales en la pantalla. La aplicación o el control dibujan las pistas visuales.

La guía del reconocedor puede constar de filas y columnas, y estas proporcionan al reconocedor un contexto mejor en el que realizar el reconocimiento. Las letras como "t" y "I" se reconocen más fácilmente cuando se usa una guía para dar contexto a la tinta. Por ejemplo, puede dibujar líneas horizontales en una pantalla que muestren el lugar en el que debe producirse la escritura (este tipo de guía solo consistiría en filas y no en columnas). Al escribir en las líneas, en lugar de un espacio arbitrario, mejora la precisión del reconocimiento.

En la guía se especifican los límites de la tinta en las coordenadas del espacio de tinta.

La propiedad [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) puede definir un cuadro que tenga el mismo tamaño que el cuadro definido por la propiedad [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .

En la siguiente ilustración se muestran los elementos de una guía de reconocimiento con dos filas y ninguna columna.

![Ilustración que muestra los elementos de la guía del reconocedor](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Además de dibujar líneas en la pantalla que muestren los usuarios en los que escribir, puede dibujar celdas en la pantalla en la que se escriben caracteres o palabras. Esto se denomina entrada de conversión boxing y es útil con algunos idiomas asiáticos. Para determinar si el reconocedor es capaz de proporcionar una entrada de conversión boxing, llame a la propiedad [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .

En la ilustración siguiente se muestra una guía de reconocedor con cuatro columnas.

![Ilustración en la que se muestra la guía del reconocedor con cuatro columnas](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Clase InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

