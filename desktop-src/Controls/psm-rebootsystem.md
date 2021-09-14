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
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167529"
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

## <a name="remarks"></a>Observaciones

Una aplicación solo debe enviar este mensaje en respuesta al mensaje de [notificación \_ PSN APPLY](psn-apply.md) o [PSN \_ KILLACTIVE.](psn-killactive.md)

Este mensaje hace que la [**función PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor \_ PSREBOOTSYSTEM  del identificador, pero solo si el usuario hace clic en el botón Aceptar para cerrar la hoja de propiedades. Es responsabilidad de la aplicación reiniciar el sistema, lo que se puede hacer mediante la [**función ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

Este mensaje reemplaza a todos los [**mensajes DE PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que preceden a él o los siguen.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

