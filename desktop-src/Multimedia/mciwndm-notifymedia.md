---
title: MCIWNDM_NOTIFYMEDIA mensaje (Vfw.h)
description: El mensaje MCIWNDM NOTIFYMEDIA notifica a la ventana primaria de una \_ aplicación que el medio ha cambiado.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa64b17fb3910e518e5b5d4318f8d988cf71f8c314f047a5f2eed1ff80cc843d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783026"
---
# <a name="mciwndm_notifymedia-message"></a>Mensaje NOTIFYMEDIA de MCIWNDM \_

El **mensaje MCIWNDM \_ NOTIFYMEDIA** notifica a la ventana primaria de una aplicación que el medio ha cambiado.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nuevo nombre de archivo. Si el medio se está cerrando, especifica una cadena null.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede habilitar la notificación de cambios en los medios especificando el estilo de ventana MCIWNDF \_ NOTIFYMEDIA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





