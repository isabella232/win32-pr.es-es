---
title: CBEM_DELETEITEM mensaje (Commctrl.h)
description: Quita un elemento de un control ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afba180ad6b714b597fe688cbaf1496b92735d8924cd6a238d56f081753fb3e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063315"
---
# <a name="cbem_deleteitem-message"></a>Mensaje \_ DELETEITEM de CBEM

Quita un elemento de un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que se va a quitar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el número de elementos restantes en el control . Si *iIndex* no es válido, el mensaje devuelve CB \_ ERR.

## <a name="remarks"></a>Comentarios

Este mensaje se asigna al mensaje de control de cuadro combinado [**CB \_ DELETESTRING**](cb-deletestring.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





