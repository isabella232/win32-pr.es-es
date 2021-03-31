---
title: Código de notificación de NM_DBLCLK (vista de lista) (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904998"
---
# <a name="nm_dblclk-list-view-notification-code"></a>NM \_ DBLCLK (vista de lista) código de notificación

Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versión 4,71](common-control-versions.md). Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información adicional sobre esta notificación. Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

El miembro **iItem** de *lParam* solo es válido si se hace clic en el icono o la etiqueta de la primera columna. Para determinar qué elemento se selecciona cuando tiene lugar un clic en otro lugar de una fila, envíe un mensaje de [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





