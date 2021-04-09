---
title: Mensaje de LB_GETCARETINDEX (Winuser. h)
description: Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple. El elemento puede estar o no seleccionado.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079718"
---
# <a name="lb_getcaretindex-message"></a>\_Mensaje lb GETCARETINDEX

Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple. El elemento puede estar o no seleccionado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero del elemento de cuadro de lista enfocado, o 0 si ningún elemento tiene el foco.

## <a name="remarks"></a>Observaciones

Este mensaje también se puede usar para obtener el índice del elemento seleccionado actualmente en un cuadro de lista de selección única.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETCARETINDEX**](lb-setcaretindex.md)
</dt> </dl>

 

 





