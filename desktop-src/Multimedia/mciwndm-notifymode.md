---
title: MCIWNDM_NOTIFYMODE mensaje (Vfw.h)
description: El mensaje MCIWNDM NOTIFYMODE notifica a la ventana primaria de una aplicación que el modo de funcionamiento del \_ dispositivo MCI ha cambiado.
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
ms.openlocfilehash: c610904512e2b39a5c0f16781c1d9f27155f7826941aebfc66fcd9259f7ee8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525425"
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

## <a name="remarks"></a>Comentarios

Puede habilitar la notificación de los cambios de modo de un dispositivo MCI especificando el estilo de ventana MCIWNDF \_ NOTIFYMODE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





