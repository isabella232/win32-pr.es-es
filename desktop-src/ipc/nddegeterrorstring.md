---
description: Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Función NDdeGetErrorString (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 728ccd283f0f65caafd6f23781bd75f18e9c796ad2fb147f00ab6350c53bfd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557045"
---
# <a name="nddegeterrorstring-function"></a>Función NDdeGetErrorString

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uErrorCode* \[ En\]
</dt> <dd>

Código de error que se va a convertir en una cadena de error.

</dd> <dt>

*lpszErrorString* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la cadena de error traducida. Este parámetro no puede ser **NULL.** Si el búfer no es lo suficientemente grande como para almacenar la cadena de error completa, la cadena se trunca.

</dd> <dt>

*cBufSize* \[ En\]
</dt> <dd>

Tamaño del búfer para recibir la cadena de error, en **TCHAR.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es cero.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero. Si el *búfer lpszErrorString* no es lo suficientemente grande como para aceptar la cadena de error completa y la cadena se trunca, la función devuelve el valor NDDE \_ INTERNAL \_ ERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) y **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




