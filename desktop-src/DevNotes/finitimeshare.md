---
description: Inicializa el recurso compartido de IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Función FInitIMEShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 178b39c67d12473663eb93bc300651341a9c459c19680218fa2c6f7a939c688c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691385"
---
# <a name="finitimeshare-function"></a>Función FInitIMEShare

Inicializa el recurso compartido de IME.

## <a name="syntax"></a>Sintaxis


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si se** ejecuta correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Se debe llamar a esta función antes de llamar a cualquier otra función de recurso compartido de IME.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EndIMEShare**](endimeshare.md)
</dt> </dl>

 

 
