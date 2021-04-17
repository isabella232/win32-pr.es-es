---
description: Se produce cuando cambia el contenido del control InkEdit.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Evento InkEdit. Change (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697562"
---
# <a name="inkeditchange-event"></a>Evento InkEdit. Change

Se produce cuando cambia el contenido del control [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintaxis


```C++
void Change();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento se produce siempre que cambia cualquier propiedad que afecte al contenido del control [InkEdit](inkedit-control-reference.md) .

Este método de evento se define en la interfaz **\_ IInkEditEvents** . La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IeeChange**.

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

 

 




