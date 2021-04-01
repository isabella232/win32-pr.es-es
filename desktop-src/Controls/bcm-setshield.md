---
title: Mensaje de BCM_SETSHIELD (commctrl. h)
description: Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la \_ macro Button SetElevationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150198"
---
# <a name="bcm_setshield-message"></a>\_Mensaje SETSHIELD de BCM

Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Valor **booleano** que es **true** para dibujar un icono elevado, o bien **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente, o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Una aplicación debe manifestarse para usar comctl32.dll versión 6 para obtener esta funcionalidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





