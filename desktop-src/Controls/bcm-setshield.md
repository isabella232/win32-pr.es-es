---
title: BCM_SETSHIELD mensaje (Commctrl.h)
description: Establece el estado requerido de elevación para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la macro \_ Button SetEintegraationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ab7ab495e713d9f2c8d58c6723489f0099a7c2cba9df93d4f08870d521a0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921495"
---
# <a name="bcm_setshield-message"></a>Mensaje \_ SETSHIELD de BCM

Establece el estado requerido de elevación para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetEintegraationRequiredState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Un **VALOR BOOL que** es TRUE **para** dibujar un icono con privilegios elevados o **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente o un código de error de lo contrario.

## <a name="remarks"></a>Comentarios

Se debe manifiesto una aplicación para usar comctl32.dll versión 6 para obtener esta funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





