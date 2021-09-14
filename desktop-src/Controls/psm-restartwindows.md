---
title: PSM_RESTARTWINDOWS mensaje (Prsht.h)
description: Indica que Windows debe reiniciarse para que los cambios suban efecto.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167517"
---
# <a name="psm_restartwindows-message"></a>MENSAJE \_ DE REINICIO DE PSMWINDOWS

Indica que Windows debe reiniciarse para que los cambios suban efecto.

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

Una aplicación debe enviar este mensaje solo en respuesta al código de notificación [PSN \_ APPLY](psn-apply.md) o [PSN \_ KILLACTIVE.](psn-killactive.md) Puede enviar el mensaje **PSM \_ RESTARTWINDOWS** explícitamente o mediante la [**macro PropSheet \_ RestartWindows.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows)

Este mensaje hace que la función [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor \_ de ID PSRESTARTWINDOWS, pero solo si el usuario hace clic en el botón Aceptar para cerrar la hoja de propiedades.  Es responsabilidad de la aplicación reiniciar Windows, lo que se puede hacer mediante la [**función ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

