---
title: Mensaje de MCIWNDM_NOTIFYMEDIA (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYMEDIA notifica a la ventana primaria de una aplicación que el medio ha cambiado.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- Mensaje de MCIWNDM_NOTIFYMEDIA de Windows multimedia
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
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802012"
---
# <a name="mciwndm_notifymedia-message"></a>MCIWNDM \_ NOTIFYMEDIA

El mensaje **MCIWNDM \_ NOTIFYMEDIA** notifica a la ventana primaria de una aplicación que el medio ha cambiado.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana de MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nuevo nombre de archivo. Si el medio se está cerrando, especifica una cadena nula.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios de medios especificando el estilo de ventana de MCIWNDF \_ NOTIFYMEDIA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





