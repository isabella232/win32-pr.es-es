---
title: PSM_SETCURSELID mensaje (Prsht.h)
description: Activa la página determinada en una hoja de propiedades basada en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167501"
---
# <a name="psm_setcurselid-message"></a>Mensaje \_ SETCURSELID de PSM

Activa la página determinada en una hoja de propiedades basada en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSelByID.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recursos de la página que se activará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana que pierde la activación recibe el código de notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN y la ventana que obtiene la activación recibe el código de [notificación \_ SETACTIVE de PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





