---
title: EM_SETUNDOLIMIT mensaje (Richedit.h)
description: Establece el número máximo de acciones que se pueden almacenar en la cola de deshacer de un control de edición enriquecido.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697525"
---
# <a name="em_setundolimit-message"></a>Mensaje \_ EM SETUNDOLIMIT

Establece el número máximo de acciones que se pueden almacenar en la cola de deshacer de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número máximo de acciones que se pueden almacenar en la cola de deshacer.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el nuevo número máximo de acciones de deshacer para el control de edición enriquecido. Este valor puede ser menor que *wParam* si la memoria está limitada.

## <a name="remarks"></a>Comentarios

De forma predeterminada, el número máximo de acciones de la cola de deshacer es 100. Si aumenta este número, debe haber suficiente memoria disponible para dar cabida al nuevo número. Para mejorar el rendimiento, establezca el límite en el menor valor posible.

Si se establece el límite en cero, se deshabilita **la característica** Deshacer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**REDO DE EM \_**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





