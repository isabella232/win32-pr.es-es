---
title: Código de notificación de TBN_DROPDOWN (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN controles de código de notificación de Windows
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
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996207"
---
# <a name="tbn_dropdown-notification-code"></a>\_Código de notificación de desplegable TBN

Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación. En este código de notificación, solo son válidos los miembros **HDR** y **iItem** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes:



| Código devuelto                                                                                          | Descripción                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_valor predeterminado de TBDDRET**</dt> </dl>      | Se controló la lista desplegable.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NOdefault**</dt> </dl>    | No se controló la lista desplegable.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | La lista desplegable se ha controlado, pero se trata el botón como un botón normal.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Los botones desplegables pueden ser sin formato (estilo [**\_ desplegable BTNS**](toolbar-control-and-button-styles.md) ), mostrar una flecha junto a la imagen del botón (estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) ) o mostrar una flecha que esté separada de la imagen (estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ). Si se usa una flecha separada, \_ la lista desplegable TBN se envía solo si el usuario hace clic en la parte de la flecha del botón. Si el usuario hace clic en la parte principal del botón, se envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el identificador del botón, al igual que con un botón estándar. En el caso de los otros dos estilos del botón desplegable, \_ se envía la lista desplegable TBN cuando el usuario hace clic en cualquier parte del botón.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

