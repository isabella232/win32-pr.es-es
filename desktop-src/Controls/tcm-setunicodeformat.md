---
title: TCM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TCM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control.'
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- TCM_SETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9192f6172505b94ad5c5312d021fea1191d376d3c7a8b02254355c33c53abe50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876225"
---
# <a name="tcm_setunicodeformat-message"></a>Mensaje \_ SETUNICODEFORMAT de TCM

Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. Puede enviar este mensaje explícitamente o usar la macro [**TabCtrl \_ SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat)

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ GETUNICODEFORMAT**](tcm-getunicodeformat.md)
</dt> </dl>

 

 





