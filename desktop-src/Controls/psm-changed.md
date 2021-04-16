---
title: Mensaje de PSM_CHANGED (Prsht. h)
description: Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658318"
---
# <a name="psm_changed-message"></a>Mensaje de PSM \_ cambiado

Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la página que ha cambiado.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La hoja de propiedades habilitará el botón **aplicar** .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





