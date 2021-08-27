---
title: MCIWNDM_SENDSTRING mensaje (Vfw.h)
description: El mensaje MCIWNDM SENDSTRING envía un comando MCI en forma de cadena al dispositivo asociado \_ a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98ee008346821c2d489b19d01bb372c37cd3d541380fd8dae3b72bf613051f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037935"
---
# <a name="mciwndm_sendstring-message"></a>Mensaje SENDSTRING de MCIWNDM \_

El **mensaje MCIWNDM \_ SENDSTRING** envía un comando MCI en forma de cadena al dispositivo asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSendString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*Sz*
</dt> <dd>

Comando String que se envía al dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

El controlador de mensajes **para MCIWNDM \_ SENDSTRING** anexa un alias de dispositivo al comando MCI que envía al dispositivo. Por lo tanto, no debe usar ningún alias en un comando MCI que emita con **MCIWNDM \_ SENDSTRING**.

Para obtener la cadena de devolución, que contiene el resultado del comando, envíe el [**mensaje \_ RETURNSTRING de MCIWNDM.**](mciwndm-returnstring.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Cadenas de comandos multimedia](multimedia-command-strings.md)
</dt> </dl>

 

 





