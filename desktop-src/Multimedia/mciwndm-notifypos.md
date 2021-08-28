---
title: MCIWNDM_NOTIFYPOS mensaje (Vfw.h)
description: El mensaje MCIWNDM NOTIFYPOS notifica a la ventana primaria de una \_ aplicación que la posición de la ventana ha cambiado.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS mensaje Windows Multimedia
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
ms.openlocfilehash: d55d3b14ffb6a42e0c41cb820e066eee5c419b069e0d92ad614ffb51d577b963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429005"
---
# <a name="mciwndm_notifypos-message"></a>Mensaje NOTIFYPOS de MCIWNDM \_

El **mensaje MCIWNDM \_ NOTIFYPOS** notifica a la ventana primaria de una aplicación que la posición de la ventana ha cambiado.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*Pos*
</dt> <dd>

Describe la nueva posición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios en la posición de una ventana de MCIWnd especificando el estilo de ventana MCIWNDF \_ NOTIFYPOS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





