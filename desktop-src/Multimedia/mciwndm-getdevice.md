---
title: Mensaje de MCIWNDM_GETDEVICE (VFW. h)
description: El \_ mensaje MCIWNDM GETDEVICE recupera el nombre del dispositivo MCI abierto actualmente. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- Mensaje de MCIWNDM_GETDEVICE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489425"
---
# <a name="mciwndm_getdevice-message"></a>MCIWNDM \_ GETDEVICE

El mensaje **MCIWNDM \_ GETDEVICE** recupera el nombre del dispositivo MCI abierto actualmente. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*terminado*
</dt> <dd>

Tamaño, en bytes, del búfer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a un búfer definido por la aplicación para devolver el nombre del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Observaciones

Si la cadena terminada en null que contiene el nombre del dispositivo es más larga que el búfer, MCIWnd lo trunca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





