---
title: Mensaje de MCIWNDM_NOTIFYMODE (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYMODE notifica a la ventana primaria de una aplicación que el modo de funcionamiento del dispositivo MCI ha cambiado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- Mensaje de MCIWNDM_NOTIFYMODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078838"
---
# <a name="mciwndm_notifymode-message"></a>MCIWNDM \_ NOTIFYMODE

El mensaje **MCIWNDM \_ NOTIFYMODE** notifica a la ventana primaria de una aplicación que el modo de funcionamiento del dispositivo MCI ha cambiado.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana de MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*modo*
</dt> <dd>

Entero que corresponde al modo MCI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de cambios de modo de un dispositivo MCI especificando el estilo de ventana de MCIWNDF \_ NOTIFYMODE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





