---
title: Código de notificación de TBN_GETBUTTONINFO (commctrl. h)
description: Recupera información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios realizados en la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996797"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>Código de notificación de GETBUTTONINFO de TBN \_

Recupera información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios realizados en la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . El miembro **iItem** especifica un índice basado en cero que proporciona un recuento de los botones que el cuadro de diálogo Personalizar barra de herramientas muestra como disponibles y presentes en la barra de herramientas. El miembro **miembros pszText** especifica la dirección del texto del botón actual y **cchText** especifica su longitud en caracteres. La aplicación debe rellenar la estructura con información acerca del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la información del botón se copió en la estructura especificada o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El control de barra de herramientas asigna un búfer y el receptor (ventana primaria) debe copiar el texto en ese búfer. El miembro **cchText** contiene la longitud del búfer asignado por la barra de herramientas cuando \_ se envía TBN GETBUTTONINFO a la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) y **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





