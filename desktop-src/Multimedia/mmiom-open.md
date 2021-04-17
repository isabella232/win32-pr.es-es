---
title: Mensaje de MMIOM_OPEN (mmsystem. h)
description: La \_ función mmioOpen envía el mensaje MMIOM Open a un procedimiento de e/s para solicitar que se abra o se elimine un archivo.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- Mensaje de MMIOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651424"
---
# <a name="mmiom_open-message"></a>MMIOM \_ abrir mensaje

La función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) envía el mensaje **MMIOM \_ Open** a un procedimiento de e/s para solicitar que se abra o se elimine un archivo.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

Cadena terminada en null que contiene el nombre del archivo que se va a abrir.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve MMSYSERR \_ NoError si se realiza correctamente o un error en caso contrario. Entre los posibles valores de error se incluyen los siguientes:



| Requisito | Value |
|--------------------|---------------------------------------------|
| MMIOM \_ CANNOTOPEN  | No se pudo abrir el archivo.               |
| MMIOM \_ OUTOFMEMORY | Memoria insuficiente para realizar la operación. |



 

## <a name="remarks"></a>Observaciones

El miembro **dwFlags** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contiene las marcas que se pasan a la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .

El miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) se inicializa en cero. Si este valor es incorrecto, el procedimiento de e/s debe corregirlo.

Si la aplicación pasa una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) a [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), el valor devuelto se devuelve en el miembro **wErrorRet** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

