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
ms.openlocfilehash: 6793aa6d0e0f3001a5c8c76b34ed6bbd1011ba17441fd709ee016d9d161a97b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525385"
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

## <a name="remarks"></a>Comentarios

Puede habilitar la notificación de cambios en el tamaño de una ventana de MCIWnd especificando el estilo de ventana MCIWNDF \_ NOTIFYSIZE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





