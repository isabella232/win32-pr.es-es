---
title: Mensaje de PSM_RECALCPAGESIZES (Prsht. h)
description: Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de que se hayan agregado o quitado páginas. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658315"
---
# <a name="psm_recalcpagesizes-message"></a>Mensaje de PSM \_ RECALCPAGESIZES

Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o del asistente después de que se hayan agregado o quitado páginas. Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .

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

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se crea una hoja de propiedades, se ajusta para ajustarse a su colección inicial de páginas. Con el fin de mantener la compatibilidad con versiones anteriores de los controles comunes, las hojas de propiedades y los asistentes no cambian de tamaño automáticamente cuando se agregan o quitan páginas posteriormente. Con los controles comunes [versión 5,80](common-control-versions.md), las aplicaciones deben enviar un mensaje de **PSM \_ RECALCPAGESIZES** después de agregar o quitar páginas con [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)o sus macros equivalentes. Garantiza que la hoja de propiedades tenga el tamaño adecuado para su colección actual de páginas. Si no se envía este mensaje, es posible que algunas páginas de hojas de propiedades estén truncadas o sean demasiado grandes.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





