---
title: MCIWNDM_NOTIFYSIZE mensaje (Vfw.h)
description: El mensaje MCIWNDM NOTIFYSIZE notifica a la ventana primaria de una \_ aplicación que el tamaño de la ventana ha cambiado.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370711"
---
# <a name="mciwndm_notifysize-message"></a>Mensaje NOTIFYSIZE de MCIWNDM \_

El **mensaje MCIWNDM \_ NOTIFYSIZE** notifica a la ventana primaria de una aplicación que el tamaño de la ventana ha cambiado.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana MCIWnd.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios en el tamaño de una ventana de MCIWnd especificando el estilo de ventana MCIWNDF \_ NOTIFYSIZE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





