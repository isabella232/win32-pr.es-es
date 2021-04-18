---
description: Finaliza el recurso compartido de IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660165"
---
# <a name="endimeshare-function"></a>EndIMEShare función)

Finaliza el recurso compartido de IME.

## <a name="syntax"></a>Sintaxis


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Se debe llamar a esta función después de que se llame a la última función de recurso compartido de IME.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FInitIMEShare**](finitimeshare.md)
</dt> </dl>

 

 
