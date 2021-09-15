---
description: Usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Función GetStringsFromBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476738"
---
# <a name="getstringsfromblob-function"></a>Función GetStringsFromBlob

La **función GetStringsFromBlob** usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*pRequestedOwnerName* \[ En\]
</dt> <dd>

Puntero a la sección Propietario de la que se obtiene la cadena.

</dd> <dt>

*pRequestedCategoryName* \[ En\]
</dt> <dd>

Puntero a la sección Categoría de la que se obtiene la cadena.

</dd> <dt>

*pRequestedTagName* \[ En\]
</dt> <dd>

Puntero a la etiqueta de la cadena solicitada.

</dd> <dt>

*ppReturnedOwnerName* \[ out\]
</dt> <dd>

Puntero a la variable que apunta a dónde **se** devolverá el nombre del propietario.

</dd> <dt>

*ppReturnedCategoryName* \[ out\]
</dt> <dd>

Puntero a la variable que apunta a dónde se devolverá **el nombre** de categoría.

</dd> <dt>

*ppReturnedTagName* \[ out\]
</dt> <dd>

Puntero a la variable que apunta a donde se devolverá **el nombre** de etiqueta.

</dd> <dt>

*ppReturnedString* \[ out\]
</dt> <dd>

Puntero a la variable que apunta a dónde se devolverá el nombre de cadena.

</dd> <dt>

*pRestartKey* \[ out\]
</dt> <dd>

Puntero a la variable donde se especificará y devolverá la clave de reinicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el problema.

Si no existe una combinación especificada  de información **de** **propietario,** categoría y etiqueta, el valor devuelto es **NMERR \_ BLOB ENTRY DOES NOT \_ \_ \_ \_ EXIST**.

Cuando el BLOB se recorre completamente dentro de los límites especificados inicialmente, la función devuelve **NMERR \_ BLOB ENTRY DOES NOT \_ \_ \_ \_ EXIST** y el parámetro *pRestartKey* apunta a cero.

## <a name="remarks"></a>Observaciones

En la llamada inicial a la **función GetStringsFromBlob,** el parámetro *pRestartKey* apunta a una variable que contiene el valor cero. Los *parámetros pRequested* solo se pueden usar cuando la clave de reinicio es cero. En las llamadas posteriores, *cuando pRestartKey* tiene valores distintos de cero, se omiten los *parámetros pRequested.* En la llamada inicial, todos pueden apuntar a **NULL,** que configura la consulta para devolver cada entrada del BLOB, una por cada llamada posterior.

La especificación de un propietario limita las cadenas devueltas solo a ese propietario. Se aplica una limitación similar a las categorías y etiquetas, con la advertencia adicional de que si se especifica una categoría, también se debe especificar un propietario y, si se especifica una etiqueta, se debe especificar una categoría (y, por tanto, un propietario).

Cuando se devuelve la llamada inicial a **GetStringsFromBlob,** *pRestartKey* apunta a un nuevo valor, que se debe especificar en la siguiente llamada a la función para obtener el siguiente valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> </dl>

 

 




