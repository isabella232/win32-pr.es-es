---
title: MMIOM_CLOSE mensaje (Mmsystem.h)
description: La función mmioClose envía el mensaje MMIOM CLOSE a un procedimiento de E/S para solicitar \_ que se cierre un archivo.
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
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371101"
---
# <a name="mmiom_close-message"></a>Mensaje MMIOM \_ CLOSE

La función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) envía el mensaje **\_ MMIOM CLOSE** a un procedimiento de E/S para solicitar que se cierre un archivo.


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

Devuelve cero si el archivo se ha cerrado correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

