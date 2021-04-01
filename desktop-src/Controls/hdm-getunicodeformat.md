---
title: Mensaje de HDM_GETUNICODEFORMAT (commctrl. h)
description: Obtiene la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetUnicodeFormat.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150315"
---
# <a name="hdm_getunicodeformat-message"></a>HDM \_ GETUNICODEFORMAT

Obtiene la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode para el control. Si este valor es distinto de cero, el control utiliza caracteres Unicode. Si este valor es cero, el control usa caracteres ANSI.

## <a name="remarks"></a>Observaciones

Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md)
</dt> </dl>

 

 





