---
title: MMIOM_CLOSE mensaje (Mmsystem.h)
description: La función mmioClose envía el mensaje MMIOM CLOSE a un procedimiento de E/S para solicitar que \_ se cierre un archivo.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065395"
---
# <a name="mmiom_close-message"></a>Mensaje CLOSE de MMIOM \_

La función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) envía el mensaje CLOSE de **\_ MMIOM** a un procedimiento de E/S para solicitar que se cierre un archivo.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Marcas contenidas en el **parámetro wFlags** de **mmioClose.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el archivo se cierra correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

