---
title: Mensaje de PSM_APPLY (Prsht. h)
description: Simula la selección del botón aplicar, que indica que una o más páginas han cambiado y los cambios deben validarse y registrarse.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905472"
---
# <a name="psm_apply-message"></a>Mensaje de aplicación de PSM \_

Simula la selección del botón **aplicar** , que indica que una o más páginas han cambiado y los cambios deben validarse y registrarse.

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

Devuelve **true** si todas las páginas aplicaron correctamente los cambios o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La hoja de propiedades envía el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) a la página actual. Si la página actual devuelve **false**, la hoja de propiedades envía [PSN \_ aplicar](psn-apply.md) código de notificación a todas las páginas activas. Puede enviar el mensaje de \_ aplicación PSM explícitamente o mediante la macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





