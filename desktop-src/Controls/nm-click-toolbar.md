---
title: Código de notificación de NM_CLICK (barra de herramientas) (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Código de notificación de NM_CLICK (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905689"
---
# <a name="nm_click-toolbar-notification-code"></a>NM \_ código de notificación de clic (barra de herramientas)

Se envía por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema. Devuelve **false** para permitir el procesamiento predeterminado del clic.

## <a name="remarks"></a>Observaciones

Al hacer clic en un elemento con el botón primario del mouse, la barra de herramientas envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) con el código de notificación en el que se [ \_ hizo clic BN](bn-clicked.md) a la ventana primaria. La notificación de clic de NM \_ se envía después del mensaje de **\_ comando de WM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

