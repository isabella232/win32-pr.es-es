---
title: Mensaje de LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtiene el ancho de una columna en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la \_ macro GetColumnWidth de ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149903"
---
# <a name="lvm_getcolumnwidth-message"></a>\_Mensaje GETCOLUMNWIDTH LVM

Obtiene el ancho de una columna en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetColumnWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna. Este parámetro se omite en la vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de columna si se realiza correctamente o cero en caso contrario. Si este mensaje se envía a un control de vista de lista con el estilo de [**\_ Informe LVS**](list-view-window-styles.md) y la columna especificada no existe, el valor devuelto es indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





