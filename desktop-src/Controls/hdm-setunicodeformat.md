---
title: HDM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'HDM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres UNICODE para el control.'
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- HDM_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32ffa5f7f90ab266c52c67899dbff3be0d51123
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085963"
---
# <a name="hdm_setunicodeformat-message"></a>Mensaje \_ SETUNICODEFORMAT de HDM

Establece la marca de formato de caracteres UNICODE para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetUnicodeFormat de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Juego de caracteres utilizado por el control . Si este valor es distinto de cero, el control usará caracteres Unicode. Si este valor es cero, el control usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode anterior para el control .

## <a name="remarks"></a>Comentarios

Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HDM \_ GETUNICODEFORMAT**](hdm-getunicodeformat.md)
</dt> </dl>

 

 





