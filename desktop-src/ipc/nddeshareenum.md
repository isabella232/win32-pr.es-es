---
description: Recupera la lista de recursos compartidos DDE disponibles.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Función NDdeShareEnum (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359159"
---
# <a name="nddeshareenum-function"></a>Función NDdeShareEnum

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera la lista de recursos compartidos DDE disponibles.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeShareEnum(
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

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*nLevel* \[ En\]
</dt> <dd>

Reservado. Este parámetro debe ser cero.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la lista de recursos compartidos de DDE. La lista de recursos compartidos de DDE se almacena como una secuencia de cadenas separadas por null que finalizan con un carácter nulo doble al final. Este parámetro puede ser **NULL**. Si *lpBuffer* es **NULL,** DSDM devuelve el tamaño de búfer necesario para contener la lista de recursos compartidos en el *parámetro lpcbTotalAvailable.*

</dd> <dt>

*cBufSize* \[ En\]
</dt> <dd>

Tamaño del búfer *lpBuffer,* en bytes. Este parámetro debe ser cero si *lpBuffer* es **NULL.**

</dd> <dt>

*lpnEntriesRead* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número total de recursos compartidos que se enumeran. Este parámetro no puede ser **NULL.**

</dd> <dt>

*lpcbTotalAvailable* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número total de bytes necesarios en el búfer para almacenar la lista de recursos compartidos de DDE. Este parámetro no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el *parámetro lpBuffer* **es NULL,** devuelve NDDE \_ BUF TOO \_ \_ SMALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareEnumW** (Unicode) y **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




