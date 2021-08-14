---
title: CBEM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: Establece la marca de formato de caracteres UNICODE para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- CBEM_SETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59730922c1d72da90e1c7ba47a287e42ce4ad40375d8216be114e7c280b5a38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699314"
---
# <a name="cbem_setunicodeformat-message"></a>Mensaje \_ SETUNICODEFORMAT de CBEM

Establece la marca de formato de caracteres UNICODE para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md)
</dt> </dl>

 

 





