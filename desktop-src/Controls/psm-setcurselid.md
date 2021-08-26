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
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877025"
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

## <a name="remarks"></a>Comentarios

La ventana que pierde la activación recibe el código de notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN y la ventana que obtiene la activación recibe el código de [notificación \_ SETACTIVE de PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





