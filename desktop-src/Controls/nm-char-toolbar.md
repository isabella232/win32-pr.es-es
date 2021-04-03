---
title: Código de notificación de NM_CHAR (barra de herramientas) (commctrl. h)
description: Se envía mediante una barra de herramientas cuando recibe un mensaje de tipo WM \_ Char. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Código de notificación de NM_CHAR (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905692"
---
# <a name="nm_char-toolbar-notification-code"></a>NM \_ Char (barra de herramientas) código de notificación

Se envía mediante una barra de herramientas cuando recibe un mensaje de tipo [**WM \_ Char**](/windows/desktop/inputdev/wm-char) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene información adicional sobre el carácter que causó el código de notificación. El miembro **dwItemPrev** de esta estructura contiene el identificador de comando del elemento activo actualmente o-1 si no hay ningún elemento activo actualmente. El miembro **dwItemNext** de esta estructura contiene el identificador de comando del elemento que volverá a estar activo o-1 si la clave no coincide con el acelerador de cualquier elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para indicar que la barra de herramientas no debe procesar el carácter y **false** para que la barra de herramientas procese el carácter.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

