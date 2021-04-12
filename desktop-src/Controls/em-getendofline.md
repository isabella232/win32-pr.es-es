---
title: Mensaje de EM_GETENDOFLINE (commctrl. h)
description: Recupera el carácter de final de línea utilizado cuando se inserta un LineBreak. Envíe este mensaje explícitamente o mediante la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489466"
---
# <a name="em_getendofline-message"></a>\_Mensaje GETENDOFLINE em

Recupera el carácter de fin de línea para un control de edición. Envíe este mensaje explícitamente o mediante la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el carácter de final de línea utilizado por el control de edición. Puede ser uno de los valores siguientes.

| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**\_CRLF ENDOFLINE \_ EC**</dt> </dl> | El carácter de final de línea usado para New saltos es el retorno de carro seguido de avance de línea (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | El carácter de final de línea usado para New saltos es el retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**\_ENDOFLINE de \_ LF de EC**</dt> </dl>       | El carácter de final de línea usado para New saltos es avance de línea (LF).<br/>                               |

## <a name="remarks"></a>Observaciones

Cuando el carácter de final de línea usado se establece en **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** con [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), este mensaje devolverá el carácter de final de línea detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETENDOFLINE em*](em-setendofline.md)
</dt> </dl>
 

 





