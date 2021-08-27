---
title: PSM_REBOOTSYSTEM mensaje (Prsht.h)
description: Indica que el sistema debe reiniciarse para que los cambios suban efecto. Puede enviar el mensaje PSM \_ REBOOTSYSTEM explícitamente o mediante la macro PropSheet \_ RebootSystem.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM controles de Windows mensaje
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
ms.openlocfilehash: dfcfebc931d1dbf01ab053fa2723bdcf361c4be5ef1443b9131115e2300770cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088635"
---
# <a name="psm_rebootsystem-message"></a>Mensaje DE \_ PSM REBOOTSYSTEM

Indica que el sistema debe reiniciarse para que los cambios suban efecto. Puede enviar el mensaje **PSM \_ REBOOTSYSTEM** explícitamente o mediante la [**macro PropSheet \_ RebootSystem.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem)

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

## <a name="remarks"></a>Comentarios

Una aplicación debe enviar este mensaje solo en respuesta al mensaje de notificación [ \_ PSN APPLY](psn-apply.md) o [PSN \_ KILLACTIVE.](psn-killactive.md)

Este mensaje hace que [**la función PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor \_ ID PSREBOOTSYSTEM, pero solo si el usuario hace clic en el botón Aceptar para cerrar la hoja de propiedades.  Es responsabilidad de la aplicación reiniciar el sistema, lo que se puede hacer mediante la [**función ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

Este mensaje reemplaza a todos los [**mensajes DE PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que preceden o siguen.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

