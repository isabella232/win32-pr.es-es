---
title: Mensaje de PSM_REBOOTSYSTEM (Prsht. h)
description: Indica que el sistema debe reiniciarse para que los cambios surtan efecto. Puede enviar el mensaje de PSM \_ REBOOTSYSTEM explícitamente o mediante la \_ macro REBOOTSYSTEM de PropSheet.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489952"
---
# <a name="psm_rebootsystem-message"></a>Mensaje de PSM \_ REBOOTSYSTEM

Indica que el sistema debe reiniciarse para que los cambios surtan efecto. Puede enviar el mensaje de **PSM \_ REBOOTSYSTEM** explícitamente o mediante la [**macro \_ REBOOTSYSTEM de PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .

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

Una aplicación debe enviar este mensaje solo en respuesta al mensaje de notificación [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .

Este mensaje hace que la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el \_ valor de identificador PSREBOOTSYSTEM, pero solo si el usuario hace clic en el botón **Aceptar** para cerrar la hoja de propiedades. Es responsabilidad de la aplicación reiniciar el sistema, lo que se puede hacer mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

Este mensaje sustituye a todos los mensajes de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que preceden o siguen.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

