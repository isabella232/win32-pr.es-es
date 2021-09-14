---
title: MCIWNDM_NOTIFYERROR mensaje (Vfw.h)
description: El mensaje NOTIFYERROR de MCIWNDM notifica a la ventana primaria de una \_ aplicación que se produjo un error de MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250851"
---
# <a name="mciwndm_notifyerror-message"></a>Mensaje NOTIFYERROR de MCIWNDM \_

El **mensaje \_ NOTIFYERROR de MCIWNDM** notifica a la ventana primaria de una aplicación que se produjo un error de MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Identificador de la ventana MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*
</dt> <dd>

Código numérico para el error de MCI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de errores de MCI especificando el estilo de ventana \_ NOTIFYERROR de MCIWNDF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





