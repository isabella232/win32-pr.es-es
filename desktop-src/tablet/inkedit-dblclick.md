---
description: Se produce cuando se hace doble clic en el control InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Evento InkEdit.DblClick (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2f1cf2a7b7d7d699af5cd8a148e5c54a2879ad5eb879bd34af7531025748e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032093"
---
# <a name="inkeditdblclick-event"></a>Evento InkEdit.DblClick

Se produce cuando se hace doble clic en el control [InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar el evento del control primario; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho e central del mouse, use los eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp.**](inkedit-mouseup.md) Si hay código en el evento [**Click,**](inkedit-click.md) el **evento DblClick** nunca se desencadenará.

 

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la interfaz IDispatch con un identificador **de DISPID \_ IeeDblClick**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




