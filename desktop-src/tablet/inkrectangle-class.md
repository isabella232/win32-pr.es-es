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
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467177"
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
| [**Inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lectura y escritura<br/> | Obtiene o establece la posición inferior del rectángulo.<br/>      |
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lectura y escritura<br/> | Obtiene o establece el acceso a la estructura del rectángulo (solo C++).<br/> |
| [**Izquierda**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lectura y escritura<br/> | Obtiene o establece la posición izquierda del rectángulo.<br/>        |
| [**Correcto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lectura y escritura<br/> | Obtiene o establece la posición derecha del rectángulo.<br/>       |
| [**Arriba**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lectura y escritura<br/> | Obtiene o establece la posición superior del rectángulo.<br/>         |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Un punto está dentro de **una inkRectangle** si se encuentra en el lado izquierdo [**o**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) superior o está dentro de los cuatro lados. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) Un punto en el [**lado derecho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) [**o inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) se considera fuera del rectángulo.

 

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

> [!Note]  
> No **se puede usar InkRectangle** si es mayor que LONG MAX \_ (2^31 - 1) en ninguna de las dimensiones.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

