---
description: Se produce cuando cambia el contenido del control InkEdit.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Evento InkEdit.Change (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3679b32b633a9983cc239fdf232491ce13b7805c053c9e1c268c84b9932586ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712975"
---
# <a name="inkeditchange-event"></a>InkEdit.Change, evento

Se produce cuando cambia el contenido del control [InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void Change();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este evento se produce siempre que cambian las propiedades que afectan al contenido del control [InkEdit.](inkedit-control-reference.md)

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la interfaz IDispatch con un identificador **de DISPID \_ IeeChange.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




