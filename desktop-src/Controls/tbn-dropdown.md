---
title: TBN_DROPDOWN de notificación (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2cdee38176b2ed72d42aaa29ca685a5e73dd30ceb7e315b5cbe0971161dc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077929"
---
# <a name="tbn_dropdown-notification-code"></a>Código de notificación DE LISTA DESPLEGABLE de TBN \_

Enviado por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación. Para este código de notificación, solo los **miembros hdr** **e iItem** de esta estructura son válidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes:



| Código devuelto                                                                                          | Descripción                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ PREDETERMINADO**</dt> </dl>      | Se controló la lista desplegable.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NODEFAULT**</dt> </dl>    | No se controló la lista desplegable.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | La lista desplegable se controló, pero trata el botón como un botón normal.<br/> |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Los botones desplegables pueden ser sin formato (estilo [**BTNS \_ DROPDOWN),**](toolbar-control-and-button-styles.md) mostrar una flecha junto a la imagen de botón (estilo [**\_ BTNS WHOLEDROPDOWN)**](toolbar-control-and-button-styles.md) o mostrar una flecha separada de la imagen (estilo [**TBSTYLE \_ EX \_ DRAWDDARROWS).**](toolbar-extended-styles.md) Si se usa una flecha separada, la lista desplegable de TBN solo se envía si el usuario hace clic en la parte \_ de flecha del botón. Si el usuario hace clic en la parte principal del botón, se envía un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) con el identificador del botón, igual que con un botón estándar. Para los otros dos estilos del botón desplegable, se envía TBN DROPDOWN cuando el usuario hace clic \_ en cualquier parte del botón.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

