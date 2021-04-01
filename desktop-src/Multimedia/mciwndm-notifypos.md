---
title: Mensaje de MCIWNDM_NOTIFYPOS (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYPOS notifica a la ventana primaria de una aplicación que ha cambiado la posición de la ventana.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- Mensaje de MCIWNDM_NOTIFYPOS de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996894"
---
# <a name="mciwndm_notifypos-message"></a>MCIWNDM \_ NOTIFYPOS

El mensaje **MCIWNDM \_ NOTIFYPOS** notifica a la ventana primaria de una aplicación que ha cambiado la posición de la ventana.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana de MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*abre*
</dt> <dd>

Describe la nueva posición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios en la posición de una ventana de MCIWnd especificando el estilo de ventana de MCIWNDF \_ NOTIFYPOS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





