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
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968739"
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

## <a name="remarks"></a>Observaciones

Se debe manifiesto una aplicación para usar comctl32.dll versión 6 para obtener esta funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





