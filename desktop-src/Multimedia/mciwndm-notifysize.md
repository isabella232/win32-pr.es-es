---
title: Mensaje de MCIWNDM_NOTIFYSIZE (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYSIZE notifica a la ventana primaria de una aplicación que el tamaño de la ventana ha cambiado.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- Mensaje de MCIWNDM_NOTIFYSIZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150170"
---
# <a name="mciwndm_notifysize-message"></a>MCIWNDM \_ NOTIFYSIZE

El mensaje **MCIWNDM \_ NOTIFYSIZE** notifica a la ventana primaria de una aplicación que el tamaño de la ventana ha cambiado.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana de MCIWnd.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios en el tamaño de una ventana de MCIWnd especificando el estilo de ventana de MCIWNDF \_ NOTIFYSIZE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





