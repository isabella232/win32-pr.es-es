---
title: Mensaje de PSM_SETCURSELID (Prsht. h)
description: Activa la página especificada en una hoja de propiedades basándose en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150754"
---
# <a name="psm_setcurselid-message"></a>Mensaje de PSM \_ SETCURSELID

Activa la página especificada en una hoja de propiedades basándose en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso de la página que se va a activar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana que está perdiendo la activación recibe el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) y la ventana que obtiene la activación recibe el código de notificación [PSN \_ SETACTIVE](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





