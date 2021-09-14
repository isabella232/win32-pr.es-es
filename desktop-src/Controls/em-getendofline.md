---
title: EM_GETENDOFLINE mensaje (Commctrl.h)
description: Recupera el carácter de fin de línea que se usa cuando se inserta un linebreak. Envíe este mensaje explícitamente o mediante la macro \_ Edit GetEndOfLine .
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062191"
---
# <a name="em_getendofline-message"></a>Mensaje \_ EM GETENDOFLINE

Recupera el carácter de fin de línea de un control de edición. Envíe este mensaje explícitamente o mediante la [**macro \_ Edit GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el carácter de fin de línea utilizado por el control de edición. Puede ser uno de los siguientes valores.

| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | El carácter de fin de línea que se usa para los nuevos pasos de línea es el retorno de carro seguido del linefeed (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | El carácter de fin de línea que se usa para los nuevos linebreaks es el retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | El carácter de fin de línea que se usa para los nuevos linebreaks es linefeed (LF).<br/>                               |

## <a name="remarks"></a>Observaciones

Cuando el carácter de fin de línea utilizado se establece en **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** mediante [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), este mensaje devolverá el carácter de fin de línea detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10, versión 1809 solo aplicaciones de escritorio\]<br/>                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 





