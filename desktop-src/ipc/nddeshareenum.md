---
description: Recupera la lista de recursos compartidos DDE disponibles.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Función NDdeShareEnum (Nddeapi. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697429"
---
# <a name="nddeshareenum-function"></a>NDdeShareEnum función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

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

Un puntero a un búfer que recibe la lista de recursos compartidos DDE. La lista de recursos compartidos DDE se almacena como una secuencia de cadenas separadas por null que finalizan con un carácter nulo doble al final. Este parámetro puede ser **NULL**. Si *lpBuffer* es **null**, el DSDM devuelve el tamaño del búfer necesario para contener la lista de recursos compartidos en el parámetro *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *lpBuffer* , en bytes. Este parámetro debe ser cero si *lpBuffer* es **null**.

</dd> <dt>

*lpnEntriesRead* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número total de recursos compartidos que se están enumerando. Este parámetro no puede ser **null**.

</dd> <dt>

*lpcbTotalAvailable* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número total de bytes necesarios en el búfer para almacenar la lista de recursos compartidos DDE. Este parámetro no puede ser **null**.

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
| Nombres Unicode y ANSI<br/>   | **NDdeShareEnumW** (Unicode) y **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




