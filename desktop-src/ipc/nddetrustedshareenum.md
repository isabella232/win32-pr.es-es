---
description: Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Función NDdeTrustedShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361248"
---
# <a name="nddetrustedshareenum-function"></a>NDdeTrustedShareEnum función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*nLevel* \[ de\]
</dt> <dd>

Reservado. Este parámetro debe ser cero.

</dd> <dt>

*lpBuffer* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe la lista de recursos compartidos DDE de confianza. La lista de recursos compartidos DDE de confianza se devuelve como una secuencia de cadenas separadas por null que finalizan con un carácter nulo doble al final. Este parámetro puede ser **NULL**. Si el valor de *lpBuffer* es **null**, el DSDM devuelve el tamaño del búfer necesario para contener la lista de recursos compartidos en el campo *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *lpBuffer* , en bytes. Este parámetro debe ser cero si *lpBuffer* es **null**.

</dd> <dt>

*lpnEntriesRead* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número total de recursos compartidos de confianza que se enumeran. Este parámetro no puede ser **null**.

</dd> <dt>

*lpcbTotalAvailable* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número total de bytes necesarios para almacenar la lista de recursos compartidos DDE de confianza. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el parámetro *lpBuffer* es **null**, devuelve NDDE \_ BUF \_ demasiado \_ pequeño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeTrustedShareEnumW** (Unicode) y **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




