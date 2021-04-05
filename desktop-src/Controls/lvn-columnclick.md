---
title: Código de notificación de LVN_COLUMNCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078934"
---
# <a name="lvn_columnclick-notification-code"></a>Código de notificación de COLUMNCLICK de LVN \_

Notifica a la ventana primaria de un control de vista de lista que se hizo clic en un encabezado de columna mientras el control de vista de lista estaba en modo de informe. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . El miembro **iItem** es-1 y el miembro **iSubItem** identifica la columna. Todos los demás miembros son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El uso de formatos de control de encabezado como la \_ casilla HDF para modificar el formato de los encabezados de columna en un control de vista de lista hace que el control envíe el código de notificación [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) en lugar de LVN \_ COLUMNCLICK cuando se hace clic en un elemento de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





