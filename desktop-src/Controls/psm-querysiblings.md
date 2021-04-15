---
title: Mensaje de PSM_QUERYSIBLINGS (Prsht. h)
description: Se envía a una hoja de propiedades, que, a continuación, reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534353"
---
# <a name="psm_querysiblings-message"></a>Mensaje de PSM \_ QUERYSIBLINGS

Se envía a una hoja de propiedades, que, a continuación, reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .

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

Devuelve el valor distinto de cero de una página de la hoja de propiedades, o bien, cero si no hay ninguna página que devuelva un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Si una página devuelve un valor distinto de cero, la hoja de propiedades no envía el mensaje a las páginas siguientes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





