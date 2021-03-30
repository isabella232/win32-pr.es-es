---
title: Mensaje de MCIWNDM_SENDSTRING (VFW. h)
description: El \_ mensaje MCIWNDM SENDSTRING envía un comando MCI en forma de cadena al dispositivo asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- Mensaje de MCIWNDM_SENDSTRING de Windows multimedia
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
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803014"
---
# <a name="mciwndm_sendstring-message"></a>MCIWNDM \_ SENDSTRING

El mensaje **MCIWNDM \_ SENDSTRING** envía un comando MCI en forma de cadena al dispositivo asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*SZ*
</dt> <dd>

Comando de cadena que se va a enviar al dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El controlador de mensajes de **MCIWNDM \_ SENDSTRING** anexa un alias de dispositivo al comando de MCI que se envía al dispositivo. Por lo tanto, no debe usar ningún alias en un comando MCI que emita con **MCIWNDM \_ SENDSTRING**.

Para obtener la cadena devuelta, que contiene el resultado del comando, envíe el [**mensaje \_ RETURNSTRING de MCIWNDM**](mciwndm-returnstring.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Cadenas de comandos multimedia](multimedia-command-strings.md)
</dt> </dl>

 

 





