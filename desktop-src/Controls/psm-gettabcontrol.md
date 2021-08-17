---
title: PSM_GETTABCONTROL mensaje (Prsht.h)
description: Recupera el identificador del control de ficha de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e26c9489dc839383552b407a16313c94e1fc3b070d93f1d59ddaf0310134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169665"
---
# <a name="psm_gettabcontrol-message"></a>Mensaje \_ GETTABCONTROL de PSM

Recupera el identificador del control de ficha de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet GetTabControl.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)

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

Devuelve el identificador al control de ficha.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





