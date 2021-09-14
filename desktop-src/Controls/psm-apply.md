---
title: PSM_APPLY mensaje (Prsht.h)
description: Simula la selección del botón Aplicar, lo que indica que una o varias páginas han cambiado y que los cambios deben validarse y grabarse.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167597"
---
# <a name="psm_apply-message"></a>Mensaje \_ DE PSM APPLY

Simula la selección del **botón** Aplicar, lo que indica que una o varias páginas han cambiado y que los cambios deben validarse y grabarse.

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

Devuelve **TRUE si** todas las páginas aplicaron correctamente los cambios o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

La hoja de propiedades envía el [código de notificación \_ KILLACTIVE de PSN](psn-killactive.md) a la página actual. Si la página actual devuelve **FALSE,** la hoja de propiedades envía el [código de notificación DE PSN \_ APPLY](psn-apply.md) a todas las páginas activas. Puede enviar el mensaje PSM \_ APPLY explícitamente o mediante la [**macro PropSheet \_ Apply.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply)

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





