---
title: Mensaje EM_SETUNDOLIMIT (RichEdit. h)
description: Establece el número máximo de acciones que pueden almacenarse en la cola de deshacer de un control Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT controles de mensajes de Windows
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
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996556"
---
# <a name="em_setundolimit-message"></a>\_Mensaje SETUNDOLIMIT em

Establece el número máximo de acciones que pueden almacenarse en la cola de deshacer de un control Rich Edit.

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

El valor devuelto es el nuevo número máximo de acciones de deshacer para el control Rich Edit. Este valor puede ser menor que *wParam* si la memoria es limitada.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el número máximo de acciones en la cola de deshacer es 100. Si aumenta este número, debe haber suficiente memoria disponible para acomodar el nuevo número. Para mejorar el rendimiento, establezca el límite en el menor valor posible.

Al establecer el límite en cero, se deshabilita la característica **Deshacer** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**de \_ em**](em-canredo.md)
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**rehacer EM \_**](em-redo.md)
</dt> <dt>

[**deshacer EM \_**](em-undo.md)
</dt> </dl>

 

 





