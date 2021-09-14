---
title: EM_GETCTFOPENSTATUS mensaje (Richedit.h)
description: Determina si el teclado Text Services Framework (TSF) está abierto o cerrado.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062196"
---
# <a name="em_getctfopenstatus-message"></a>Mensaje \_ EM GETCTFOPENSTATUS

Determina si el teclado Text Services Framework (TSF) está abierto o cerrado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el teclado TSF está abierto, el valor devuelto es **TRUE.** De lo contrario, es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETCTFOPENSTATUS**](em-setctfopenstatus.md)
</dt> </dl>

 

 





