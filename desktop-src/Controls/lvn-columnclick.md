---
title: LVN_COLUMNCLICK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072322"
---
# <a name="lvn_columnclick-notification-code"></a>Código de notificación \_ LVN COLUMNCLICK

Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El **miembro iItem** es -1 y el **miembro iSubItem** identifica la columna. Todos los demás miembros son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El uso de formatos de control de encabezado como HDF CHECKBOX para modificar el formato de los encabezados de columna en un control de vista de lista hace que el control envíe el código de notificación \_ [ \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) de HDN en lugar de LVN COLUMNCLICK cuando se hace clic en un elemento de \_ encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





