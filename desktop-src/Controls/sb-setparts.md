---
title: Mensaje de SB_SETPARTS (commctrl. h)
description: Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534822"
---
# <a name="sb_setparts-message"></a>\_Mensaje SETPARTS de SB

Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se van a establecer (no puede ser mayor que 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros. El número de elementos se especifica en *wParam*. Cada elemento especifica la posición, en coordenadas de cliente, del borde derecho de la parte correspondiente. Si un elemento es-1, el borde derecho de la parte correspondiente se extiende hasta el borde de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





