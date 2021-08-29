---
title: MMIOM_OPEN mensaje (Mmsystem.h)
description: La función mmioOpen envía el mensaje MMIOM OPEN a un procedimiento de E/S para solicitar que se abra \_ o elimine un archivo.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN mensaje Windows Multimedia
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
ms.openlocfilehash: 74cb4c54a7f35fe426cf528d5eb9e076a44bf4b7e06744628ba65fe1bf7cb410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065375"
---
# <a name="mmiom_open-message"></a>Mensaje MMIOM \_ OPEN

La función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) envía el mensaje **\_ MMIOM OPEN** a un procedimiento de E/S para solicitar que se abra o elimine un archivo.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

Cadena terminada en NULL que contiene el nombre del archivo que se abrirá.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve MMSYSERR \_ NOERROR si se realiza correctamente o un error en caso contrario. Entre los posibles valores de error se incluyen los siguientes:



| Requisito | Value |
|--------------------|---------------------------------------------|
| MMIOM \_ CANNOTOPEN  | No se pudo abrir el archivo.               |
| MMIOM \_ OUTOFMEMORY | No hay suficiente memoria para realizar la operación. |



 

## <a name="remarks"></a>Comentarios

El **miembro dwFlags** de la [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contiene marcas que se pasan a la [**función mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)

El **miembro lDiskOffset** de la [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) se inicializa en cero. Si este valor es incorrecto, el procedimiento de E/S debe corregirlo.

Si la aplicación pasó una [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) a [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), el valor devuelto se devuelve en el **miembro wErrorRet.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

