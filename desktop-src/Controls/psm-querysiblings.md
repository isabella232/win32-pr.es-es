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
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088655"
---
# <a name="psm_querysiblings-message"></a>PSM \_ QUERYSIBLINGS message

Se envía a una hoja de propiedades, que luego reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ QuerySiblings.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)

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

## <a name="remarks"></a>Comentarios

Si una página devuelve un valor distinto de cero, la hoja de propiedades no envía el mensaje a las páginas posteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





