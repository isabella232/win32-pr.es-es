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
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167570"
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

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





