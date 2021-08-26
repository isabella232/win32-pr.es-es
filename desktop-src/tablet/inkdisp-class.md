---
description: 'Clase InkDisp: representa los trazos de entrada de lápiz recopilados dentro de un espacio de entrada de lápiz.'
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Clase InkDisp (Msyecciónut.h)
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
ms.openlocfilehash: 928bda8af246b41bab2c285a5292155917ba8903c6dd71c20177dbf906c64924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939165"
---
# <a name="inkdisp-class"></a>InkDisp (clase)

Representa los trazos de lápiz recopilados dentro de un espacio de entrada de lápiz.

**InkDisp** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

La **clase InkDisp** tiene estos eventos.



| Evento                                    | Descripción                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Se produce cuando se agrega un trazo al **objeto InkDisp.**<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Se produce cuando se elimina un trazo del **objeto InkDisp.**<br/> |



 

### <a name="interfaces"></a>Interfaces

La **clase InkDisp** define estas interfaces.



| Interfaz    | Descripción                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Este objeto implementa la **interfaz COM IInkDisp.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkDisp** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Inserta una colección de trazos en el **objeto InkDisp** en el rectángulo especificado.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indica si el [**objeto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) se puede convertir en un **objeto InkDisp.**<br/>                                                                                       |
| [**Clip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Quita partes de un trazo o colección de trazos que están fuera de un rectángulo.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copia la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) en el Portapapeles.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copia los [**objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenidos en el rectángulo conocido en el Portapapeles.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copia el [**objeto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) del Portapapeles en el **objeto InkDisp.**<br/>                                                                                               |
| [**Clon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Crea un objeto **InkDisp** duplicado.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Crea un trazo a partir de puntos o datos de paquetes.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Crea una [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para este **objeto InkDisp.**<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Elimina un trazo del **objeto InkDisp.**<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Elimina los trazos del **objeto InkDisp.**<br/>                                                                                                                                              |
| [**ExtractStrokes (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrae trazos del **objeto InkDisp** y devuelve un nuevo objeto **InkDisp** que contiene los trazos extraídos.<br/>                                                                       |
| [**ExtractWithRectangle (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Corta o copia trazos de un objeto de clase **InkDisp** existente y los pega en un nuevo objeto **InkDisp Class,** mediante el rectángulo conocido para determinar qué trazos extraer.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Recupera el cuadro de límite de todos los trazos del **objeto InkDisp.**<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Recupera la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está completamente dentro o está intersecda por un círculo conocido.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Recupera los trazos dentro de un área de selección de polilínea.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Recupera los trazos contenidos en un rectángulo especificado.<br/>                                                                                                                    |
| [**Cargar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Rellena un nuevo objeto **InkDisp** con datos binarios conocidos.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Recupera [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dentro del objeto **InkDisp** más cercano a un punto conocido y, opcionalmente, proporciona información adicional.<br/>                       |
| [**Guardar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Convierte la entrada de lápiz a un formato especificado y devuelve los datos binarios.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propiedades

La **clase InkDisp** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Solo lectura<br/>  | Obtiene la [**colección IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) que se va a conservar con la entrada de lápiz.<br/>                             |
| [**Sucio**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lectura/escritura<br/> | Obtiene o establece el valor que indica si se ha modificado un objeto **InkDisp** desde la última vez que se guardó la entrada manuscrita.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Solo lectura<br/>  | Obtiene la colección de datos definidos por la aplicación.<br/>                                                                             |
| [**Trazos**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Solo lectura<br/>  | Obtiene la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenida en el **objeto InkDisp.**<br/>                             |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> La primera creación de instancias de este objeto hace GDI+ crear instancias de este objeto. Un efecto secundario es que si usa un único objeto de entrada de lápiz en un bucle y lo crea y destruye dentro del bucle, hará que se cree una instancia de GDI+ una y otra vez. Esto puede provocar una degradación del rendimiento en la aplicación. Para evitarlo, mantenga una única instancia de un objeto de entrada de lápiz en todo momento mientras la aplicación usa la entrada de lápiz.

 

Un **objeto InkDisp** es un contenedor de datos de trazo (punto). Los datos de trazo, o los puntos recopilados por el lápiz, se ponen en un **objeto InkDisp.** La [**propiedad Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene los datos de todos los trazos dentro del **objeto InkDisp.**

El [**objeto InkCollector,**](inkcollector-class.md) [**el objeto InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) recopilan puntos del dispositivo de entrada y los coloca en un **objeto InkDisp.** Estos objetos actúan básicamente como el origen que distribuye la entrada de lápiz en uno o varios objetos **InkDisp** diferentes, que actúan como contenedores que mantienen la entrada manuscrita distribuida.

El espacio de entrada de lápiz es un espacio de coordenadas virtual al que se asignan las coordenadas del contexto de la tableta. Este espacio se fija en un sistema de coordenadas HIMETRIC. En coordenadas de espacio de entrada de lápiz, un movimiento de 0 a 1 equivale a 1 unidad HIMETRIC. Esta asignación facilita la relación de varios **objetos InkDisp.**

El [**objeto InkRenderer**](inkrenderer-class.md) administra las asignaciones entre la entrada manuscrita y la ventana de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**IInkTablet (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

