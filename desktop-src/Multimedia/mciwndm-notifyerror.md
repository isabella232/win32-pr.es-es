---
title: Mensaje de MCIWNDM_NOTIFYERROR (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYERROR notifica a la ventana primaria de una aplicación que se ha producido un error de MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- Mensaje de MCIWNDM_NOTIFYERROR de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079243"
---
# <a name="mciwndm_notifyerror-message"></a>MCIWNDM \_ NOTIFYERROR

El mensaje **MCIWNDM \_ NOTIFYERROR** notifica a la ventana primaria de una aplicación que se ha producido un error de MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*identificador*
</dt> <dd>

Identificador de la ventana de MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*
</dt> <dd>

Código numérico para el error de MCI.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede habilitar la notificación de error de MCI especificando el \_ estilo de ventana de MCIWNDF NOTIFYERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





