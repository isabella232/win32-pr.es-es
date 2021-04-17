---
description: Se produce cuando un usuario hace clic en el control InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. click (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688300"
---
# <a name="inkeditclick-event"></a>Evento InkEdit. click

Se produce cuando un usuario hace clic en el control [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintaxis


```C++
void Click();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Al hacer clic en un control, se generan eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp**](inkedit-mouseup.md) además del evento click.

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp**](inkedit-mouseup.md) .

 

Si hay código en el evento **click** , el evento [**DblClick**](inkedit-dblclick.md) nunca se desencadenará, porque el evento **click** es el primer evento que se va a desencadenar entre los dos. Como resultado, el evento **click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick** .

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IeeClick**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




