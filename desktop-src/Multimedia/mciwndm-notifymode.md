---
title: MCIWNDM_NOTIFYMODE mensaje (Vfw.h)
description: El mensaje NOTIFYMODE de MCIWNDM notifica a la ventana primaria de una aplicación que el modo de funcionamiento del \_ dispositivo MCI ha cambiado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370705"
---
# <a name="mciwndm_notifymode-message"></a>Mensaje NOTIFYMODE de MCIWNDM \_

El **mensaje \_ NOTIFYMODE de MCIWNDM** notifica a la ventana primaria de una aplicación que el modo de funcionamiento del dispositivo MCI ha cambiado.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modo*
</dt> <dd>

Entero correspondiente al modo MCI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de los cambios de modo de un dispositivo MCI especificando el estilo de ventana MCIWNDF \_ NOTIFYMODE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





