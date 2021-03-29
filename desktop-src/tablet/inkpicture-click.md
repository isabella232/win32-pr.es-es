---
description: Se produce cuando un usuario hace clic en el control InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture. click (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912346"
---
# <a name="inkpictureclick-event"></a>InkPicture. click (evento)

Se produce cuando un usuario hace clic en el control [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Sintaxis


```C++
void Click();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Al hacer clic en un control, se generan eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) además del evento click.

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) .

 

Si hay código en el evento **click** , el evento [**DblClick**](inkpicture-dblclick.md) nunca se desencadenará, porque el evento **click** es el primer evento que se va a desencadenar entre los dos. Como resultado, el evento **click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick** .

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEClick**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




