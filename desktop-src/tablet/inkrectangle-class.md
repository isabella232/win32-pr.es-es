---
description: Representa el acceso a un rectángulo.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Clase InkRectangle (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717160"
---
# <a name="inkrectangle-class"></a>Clase InkRectangle

Representa el acceso a un rectángulo.

**InkRectangle** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La clase **InkRectangle** define estas interfaces.



| Interfaz         | Descripción                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | Este objeto implementa la interfaz com **IInkRectangle** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkRectangle** tiene estos métodos.



| Método                                            | Descripción                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Recupera los elementos del objeto **InkRectangle** en una sola llamada.<br/> |
| [**SetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Modifica los elementos del objeto **InkRectangle** en una sola llamada.<br/>  |



 

### <a name="properties"></a>Propiedades

La clase **InkRectangle** tiene estas propiedades.



| Propiedad                                         | Tipo de acceso           | Descripción                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Bottom**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lectura/escritura<br/> | Obtiene o establece la posición inferior del rectángulo.<br/>      |
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lectura/escritura<br/> | Obtiene o establece el acceso a la estructura de rectángulo (solo C++).<br/> |
| [**Salido**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lectura/escritura<br/> | Obtiene o establece la posición izquierda del rectángulo.<br/>        |
| [**Correcta**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lectura/escritura<br/> | Obtiene o establece la posición derecha del rectángulo.<br/>       |
| [**Arriba**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lectura/escritura<br/> | Obtiene o establece la posición superior del rectángulo.<br/>         |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Un punto está dentro de un **InkRectangle** si se encuentra en el lado [**izquierdo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) o [**superior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) o en los cuatro lados. Un punto en el lado [**derecho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) o [**inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) se considera fuera del rectángulo.

 

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

> [!Note]  
> No se puede usar un **InkRectangle** si es mayor que el \_ máximo largo (2 ^ 31-1) en cualquiera de las dimensiones.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

