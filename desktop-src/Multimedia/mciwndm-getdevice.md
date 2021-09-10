---
title: MCIWNDM_GETDEVICE mensaje (Vfw.h)
description: El mensaje GETDEVICE de MCIWNDM \_ recupera el nombre del dispositivo MCI abierto actualmente. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370639"
---
# <a name="mciwndm_getdevice-message"></a>Mensaje GETDEVICE de MCIWNDM \_

El **mensaje \_ GETDEVICE de MCIWNDM** recupera el nombre del dispositivo MCI abierto actualmente. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDevice.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice)


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a un búfer definido por la aplicación para devolver el nombre del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un valor distinto de cero de lo contrario.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en NULL que contiene el nombre del dispositivo es mayor que el búfer, MCIWnd la trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





