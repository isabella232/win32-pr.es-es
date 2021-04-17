---
title: Mensaje de CBEM_DELETEITEM (commctrl. h)
description: Quita un elemento de un control ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM controles de mensajes de Windows
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
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658395"
---
# <a name="cbem_deleteitem-message"></a>Mensaje de CBEM \_ DELETEITEM

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

Devuelve un valor INT que representa el número de elementos que quedan en el control. Si *iIndex* no es válido, el mensaje devuelve un \_ error CB.

## <a name="remarks"></a>Observaciones

Este mensaje se asigna al mensaje de control de cuadro combinado [**CB \_ DELETESTRING**](cb-deletestring.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





