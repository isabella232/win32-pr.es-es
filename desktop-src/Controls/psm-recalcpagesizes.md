---
title: PSM_RECALCPAGESIZES mensaje (Prsht.h)
description: Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de agregar o quitar páginas. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167522"
---
# <a name="psm_recalcpagesizes-message"></a>Mensaje \_ PSM RECALCPAGESIZES

Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de agregar o quitar páginas. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ RecalcPageSizes.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes)

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

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se crea una hoja de propiedades, su tamaño se ajusta a su colección inicial de páginas. Para mantener la compatibilidad con versiones anteriores de los controles comunes, las hojas de propiedades y los asistentes no cambian automáticamente de tamaño cuando las páginas se agregan o quitan posteriormente. Con los controles comunes versión [5.80,](common-control-versions.md)las aplicaciones deben enviar un mensaje **\_ PSM RECALCPAGESIZES** después de agregar o quitar páginas con [**PSM \_ ADDPAGE,**](psm-addpage.md) [**PSM \_ INSERTPAGE,**](psm-insertpage.md) [**PSM \_ REMOVEPAGE**](psm-removepage.md)o sus macros equivalentes. Garantiza que la hoja de propiedades tiene el tamaño adecuado para su colección actual de páginas. Si no se envía este mensaje, algunas páginas de la hoja de propiedades pueden truncarse o ser demasiado grandes.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





