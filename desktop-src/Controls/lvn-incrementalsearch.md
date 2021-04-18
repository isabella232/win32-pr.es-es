---
title: Código de notificación de LVN_INCREMENTALSEARCH (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658420"
---
# <a name="lvn_incrementalsearch-notification-code"></a>LVN \_ código de notificación INCREMENTALSEARCH

Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que describe el código de notificación. El autor de la llamada es responsable de la asignación de esta estructura, incluidas las estructuras [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) y [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenidas. Establezca los miembros de la estructura **NMHDR** . El miembro de **código** debe establecerse en LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . El parámetro *wParam* contiene el identificador del control que envía este código de notificación.

Este código de notificación proporciona a una aplicación (o al receptor de notificaciones) la oportunidad de personalizar una búsqueda incremental. Por ejemplo, si los elementos de búsqueda son numéricos, la aplicación puede realizar una búsqueda numérica en lugar de una búsqueda de cadena.

La aplicación establece el miembro **lParam** de la estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) incluida en la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) en el resultado de la búsqueda, o en otro valor definido por la aplicación para que no se realice la búsqueda e indique al control cómo proceder.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl>   |
| Nombres Unicode y ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) y **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





