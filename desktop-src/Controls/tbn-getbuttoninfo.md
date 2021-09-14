---
title: TBN_GETBUTTONINFO de notificación (Commctrl.h)
description: Recupera la información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios que se realizan en la barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166361"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>Código de notificación \_ GETBUTTONINFO de TBN

Recupera la información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios que se realizan en la barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) El **miembro iItem** especifica un índice de base cero que proporciona un recuento de los botones que el cuadro de diálogo Personalizar barra de herramientas muestra como disponibles y presentes en la barra de herramientas. El **miembro pszText** especifica la dirección del texto del botón actual y **cchText** especifica su longitud en caracteres. La aplicación debe rellenar la estructura con información sobre el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** la información del botón se copió en la estructura especificada o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El control de barra de herramientas asigna un búfer y el receptor (ventana primaria) debe copiar el texto en ese búfer. El **miembro cchText** contiene la longitud del búfer asignado por la barra de herramientas cuando TBN \_ GETBUTTONINFO se envía a la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) y **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





