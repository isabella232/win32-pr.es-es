---
description: Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Función NDdeGetErrorString (Nddeapi. h)
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
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081981"
---
# <a name="nddegeterrorstring-function"></a>NDdeGetErrorString función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

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

*uErrorCode* \[ de\]
</dt> <dd>

Código de error que se va a convertir en una cadena de error.

</dd> <dt>

*lpszErrorString* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe la cadena de error traducida. Este parámetro no puede ser **null**. Si el búfer no es lo suficientemente grande como para almacenar la cadena de error completa, se trunca la cadena.

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño del búfer para recibir la cadena de error, en **TCHARs**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es cero.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero. Si el búfer de *lpszErrorString* no es lo suficientemente grande como para aceptar la cadena de error completa y se trunca la cadena, la función devuelve el valor NDDE \_ \_ error interno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) y **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




