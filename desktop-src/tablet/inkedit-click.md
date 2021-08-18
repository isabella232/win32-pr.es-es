---
description: Se produce cuando un usuario hace clic en el control InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit.Click (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f126035319c5d225da3fe57e075044c50f91f928277de89fce8e516e4723c701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718143"
---
# <a name="inkeditclick-event"></a>InkEdit.Click, evento

Se produce cuando un usuario hace clic en el control [InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void Click();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Al hacer clic en un control se [**generan eventos MouseDown**](inkedit-mousedown.md) [**y MouseUp**](inkedit-mouseup.md) además del evento Click.

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho e central del mouse, use los eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp.**](inkedit-mouseup.md)

 

Si hay código en el evento **Click,** el evento [**DblClick**](inkedit-dblclick.md) nunca se desencadenará, porque el evento **Click** es el primer evento que se desencadena entre los dos. Como resultado, el evento **Click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick.**

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la interfaz IDispatch con un identificador **de DISPID \_ IeeClick**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




