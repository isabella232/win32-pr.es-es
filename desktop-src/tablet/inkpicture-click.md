---
description: Se produce cuando un usuario hace clic en el control InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture.Click (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256593"
---
# <a name="inkpictureclick-event"></a>Evento InkPicture.Click

Se produce cuando un usuario hace clic en el control [InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void Click();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Al hacer clic en un control se [**generan eventos MouseDown**](inkpicture-mousedown.md) [**y MouseUp**](inkpicture-mouseup.md) además del evento Click.

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho y central del mouse, use los eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp.**](inkpicture-mouseup.md)

 

Si hay código en el evento **Click,** el evento [**DblClick**](inkpicture-dblclick.md) nunca se desencadenará, porque el evento **Click** es el primer evento que se desencadena entre los dos. Como resultado, el evento **Click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick.**

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la interfaz IDispatch con un identificador **de DISPID \_ IPEClick.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




