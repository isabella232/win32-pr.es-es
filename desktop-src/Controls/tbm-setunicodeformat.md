---
title: Mensaje de TBM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adb64c8fcb3464067e9522695930f4f9d0771357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656497"
---
# <a name="tbm_setunicodeformat-message"></a>TBM \_ SETUNICODEFORMAT

Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina el juego de caracteres utilizado por el control. Si este valor es distinto de cero, el control usará caracteres Unicode. Si este valor es cero, el control usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode anterior para el control.

## <a name="remarks"></a>Observaciones

Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md)
</dt> </dl>

 

 





