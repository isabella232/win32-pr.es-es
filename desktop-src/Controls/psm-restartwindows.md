---
title: Mensaje de PSM_RESTARTWINDOWS (Prsht. h)
description: Indica que es necesario reiniciar Windows para que los cambios surtan efecto.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905170"
---
# <a name="psm_restartwindows-message"></a>Mensaje de PSM \_ RESTARTWINDOWS

Indica que es necesario reiniciar Windows para que los cambios surtan efecto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación debe enviar este mensaje solo en respuesta al código de notificación [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) . Puede enviar el mensaje de **PSM \_ RESTARTWINDOWS** explícitamente o mediante la [**macro \_ RESTARTWINDOWS de PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .

Este mensaje hace que la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el \_ valor de identificador PSRESTARTWINDOWS, pero solo si el usuario hace clic en el botón **Aceptar** para cerrar la hoja de propiedades. Es responsabilidad de la aplicación reiniciar Windows, lo que se puede hacer mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

