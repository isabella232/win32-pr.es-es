---
title: Mensaje EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica el estado actual de las opciones bidireccionales en el control Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150408"
---
# <a name="em_getbidioptions-message"></a>\_Mensaje GETBIDIOPTIONS em

Indica el estado actual de las opciones bidireccionales en el control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Una estructura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que recibe el estado actual de las opciones bidireccionales en el control Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje establece los valores de los miembros **wMask** y **wEffects** en el valor del estado actual de las opciones bidireccionales en el control Rich Edit.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_SETBIDIOPTIONS em**](em-setbidioptions.md)
</dt> </dl>

 

 





