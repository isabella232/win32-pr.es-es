---
title: TBM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TBM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.'
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT mensaje Controles de Windows
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
ms.openlocfilehash: f076efe2a575eff131c9bc2a1fe3df9ecab0fe68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104043"
---
# <a name="tbm_setunicodeformat-message"></a>Mensaje \_ TBM SETUNICODEFORMAT

Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina el juego de caracteres utilizado por el control . Si este valor es distinto de cero, el control usará caracteres Unicode. Si este valor es cero, el control usará caracteres ANSI.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md)
</dt> </dl>

 

 





