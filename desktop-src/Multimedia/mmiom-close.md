---
title: Mensaje de MMIOM_CLOSE (mmsystem. h)
description: La \_ función mmioClose envía el mensaje de cierre MMIOM a un procedimiento de e/s para solicitar que se cierre un archivo.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Mensaje de MMIOM_CLOSE de Windows multimedia
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
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535620"
---
# <a name="mmiom_close-message"></a>MMIOM \_ cerrar mensaje

La función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) envía el mensaje de **\_ cierre MMIOM** a un procedimiento de e/s para solicitar que se cierre un archivo.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Marcas contenidas en el parámetro **wFlags** de **mmioClose**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el archivo se cierra correctamente o si se muestra un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

