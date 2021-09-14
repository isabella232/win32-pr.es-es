---
title: PSM_QUERYSIBLINGS mensaje (Prsht.h)
description: Se envía a una hoja de propiedades, que luego reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167533"
---
# <a name="psm_querysiblings-message"></a>PSM \_ QUERYSIBLINGS message

Se envía a una hoja de propiedades, que luego reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ QuerySiblings.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Primer parámetro definido por la aplicación.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parámetro definido por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor distinto de cero de una página de la hoja de propiedades o cero si ninguna página devuelve un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Si una página devuelve un valor distinto de cero, la hoja de propiedades no envía el mensaje a las páginas posteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





