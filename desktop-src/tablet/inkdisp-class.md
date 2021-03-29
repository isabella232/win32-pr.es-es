---
description: Representa los trazos recopilados de la entrada de lápiz dentro de un espacio de tinta.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Clase InkDisp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808809"
---
# <a name="inkdisp-class"></a>Clase InkDisp

Representa los trazos recopilados de la entrada de lápiz dentro de un espacio de tinta.

**InkDisp** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

La clase **InkDisp** tiene estos eventos.



| Evento                                    | Descripción                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Se produce cuando se agrega un trazo al objeto **InkDisp** .<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Se produce cuando se elimina un trazo del objeto **InkDisp** .<br/> |



 

### <a name="interfaces"></a>Interfaces

La clase **InkDisp** define estas interfaces.



| Interfaz    | Descripción                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Este objeto implementa la interfaz com **IInkDisp** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkDisp** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Inserta una colección de trazos en el objeto **InkDisp** en el rectángulo especificado.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indica si [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) se puede convertir en un objeto **InkDisp** .<br/>                                                                                       |
| [**Secuencia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Quita las partes de un trazo o de una colección de trazos que están fuera de un rectángulo.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copia la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) en el portapapeles.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copia en el portapapeles los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenidos en el rectángulo conocido.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copia [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) del portapapeles en el objeto **InkDisp** .<br/>                                                                                               |
| [**Clonar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Crea un objeto **InkDisp** duplicado.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Crea un trazo a partir de puntos o datos de paquetes.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Crea una colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para este objeto **InkDisp** .<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Elimina un trazo del objeto **InkDisp** .<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Elimina los trazos del objeto **InkDisp** .<br/>                                                                                                                                              |
| [**Método ExtractStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrae los trazos del objeto **InkDisp** y devuelve un nuevo objeto **InkDisp** que contiene los trazos extraídos.<br/>                                                                       |
| [**Método ExtractWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Corta o copia trazos de un objeto de **clase InkDisp** existente y los pega en un nuevo objeto de **clase InkDisp** , utilizando el rectángulo conocido para determinar qué trazos se van a extraer.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Recupera el rectángulo de selección de todos los trazos del objeto **InkDisp** .<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Recupera la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está completamente dentro o intersectada por un círculo conocido.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Recupera los trazos dentro de un área de selección de polilínea.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Recupera los trazos contenidos dentro de un rectángulo especificado.<br/>                                                                                                                    |
| [**Cargar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Rellena un nuevo objeto **InkDisp** con datos binarios conocidos.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Recupera el [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en el objeto **InkDisp** más cercano a un punto conocido y, opcionalmente, proporciona información adicional.<br/>                       |
| [**Guardar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Convierte la entrada de lápiz en un formato especificado y devuelve los datos binarios.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propiedades

La clase **InkDisp** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Solo lectura<br/>  | Obtiene la colección [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) que se va a conservar con la tinta.<br/>                             |
| [**OnDirty**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lectura/escritura<br/> | Obtiene o establece el valor que indica si un objeto **InkDisp** se ha modificado desde la última vez que se guardó la entrada de lápiz.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Solo lectura<br/>  | Obtiene la colección de datos definidos por la aplicación.<br/>                                                                             |
| [**Trazos**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Solo lectura<br/>  | Obtiene la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenida en el objeto **InkDisp** .<br/>                             |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> La primera instancia de este objeto hace que se creen instancias de GDI+ también. Un efecto secundario es que si usa un solo objeto de entrada de lápiz en un bucle y lo crea y destruye dentro del bucle, hará que se creen instancias de GDI+ una y otra vez. Esto puede producir una degradación del rendimiento en la aplicación. Para evitar esto, conserve una única instancia de un objeto de entrada manuscrita en todo momento mientras la aplicación usa la tinta.

 

Un objeto **InkDisp** es un contenedor de datos de trazo (punto). Los datos del trazo, o los puntos recopilados por el lápiz, se colocan en un objeto **InkDisp** . La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene los datos de todos los trazos dentro del objeto **InkDisp** .

El objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) recopilan puntos del dispositivo de entrada y los coloca en un objeto **InkDisp** . Estos objetos actúan esencialmente como el origen que distribuye la entrada manuscrita en uno o varios objetos **InkDisp** diferentes, que actúan como contenedores que contienen la tinta distribuida.

El espacio de la tinta es un espacio de coordenadas virtual al que se asignan las coordenadas del contexto de la tableta. Este espacio se fija en un sistema de coordenadas HIMETRIC. En las coordenadas de espacio de tinta, un desplazamiento de 0 a 1 es igual a 1 unidad HIMETRIC. Esta asignación facilita la relación de varios objetos **InkDisp** .

El objeto [**InkRenderer**](inkrenderer-class.md) administra las asignaciones entre la entrada de lápiz y la ventana de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Interfaz IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

