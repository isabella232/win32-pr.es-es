---
title: PSM_CHANGED mensaje (Prsht.h)
description: Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167593"
---
# <a name="psm_changed-message"></a>Mensaje PSM \_ CHANGED

Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ Changed.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed)

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

La hoja de propiedades habilitará el **botón** Aplicar.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





