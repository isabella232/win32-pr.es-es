---
description: Se produce cuando la selección actual de texto en el control InkEdit ha cambiado o se ha movido el punto de inserción.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit.SelChange (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712655"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit.SelChange

Se produce cuando la selección actual de texto en el control [InkEdit](inkedit-control-reference.md) ha cambiado o se ha movido el punto de inserción.

## <a name="syntax"></a>Sintaxis


```C++
void SelChange();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Puede usar el evento **SelChange** para comprobar las distintas propiedades que dan información sobre la selección actual (por [**ejemplo, SelBold)**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)para poder actualizar los botones de una barra de herramientas, por ejemplo.

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

 

 




