---
description: Representa el acceso a un rectángulo.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Clase InkRectangle (Msyecciónut.h)
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
ms.openlocfilehash: 808b04d7f7b7a50dc8a44ef87dccee38470509309c6e82bde5701b30049bd210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938755"
---
# <a name="inkrectangle-class"></a>InkRectangle (clase)

Representa el acceso a un rectángulo.

**InkRectangle** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La **clase InkRectangle** define estas interfaces.



| Interfaz         | Descripción                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | Este objeto implementa la **interfaz COM IInkRectangle.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkRectangle** tiene estos métodos.



| Método                                            | Descripción                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Recupera los elementos del objeto **InkRectangle** en una sola llamada.<br/> |
| [**SetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Modifica los elementos del objeto **InkRectangle** en una sola llamada.<br/>  |



 

### <a name="properties"></a>Propiedades

La **clase InkRectangle** tiene estas propiedades.



| Propiedad                                         | Tipo de acceso           | Descripción                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lectura/escritura<br/> | Obtiene o establece la posición inferior del rectángulo.<br/>      |
| [**Datos**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lectura/escritura<br/> | Obtiene o establece el acceso a la estructura de rectángulo (solo C++).<br/> |
| [**Izquierda**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lectura/escritura<br/> | Obtiene o establece la posición izquierda del rectángulo.<br/>        |
| [**Correcto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lectura/escritura<br/> | Obtiene o establece la posición derecha del rectángulo.<br/>       |
| [**Arriba**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lectura/escritura<br/> | Obtiene o establece la posición superior del rectángulo.<br/>         |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Un punto está dentro de **inkRectangle** si se encuentra en el lado izquierdo [**o**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) superior o está dentro de los cuatro lados. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) Un punto en el [**lado derecho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) [**o inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) se considera fuera del rectángulo.

 

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

> [!Note]  
> No **se puede usar inkRectangle** si es mayor que LONG MAX \_ (2^31 - 1) en cualquier dimensión.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

