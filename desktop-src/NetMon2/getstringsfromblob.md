---
description: Usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Función GetStringsFromBlob (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000921"
---
# <a name="getstringsfromblob-function"></a>GetStringsFromBlob función)

La función **GetStringsFromBlob** usa llamadas secuenciales para recuperar todas las cadenas dentro de los intervalos especificados.

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

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*pRequestedOwnerName* \[ de\]
</dt> <dd>

Un puntero a la sección del propietario de la que se va a obtener la cadena.

</dd> <dt>

*pRequestedCategoryName* \[ de\]
</dt> <dd>

Un puntero a la sección de categoría de la que se va a obtener la cadena.

</dd> <dt>

*pRequestedTagName* \[ de\]
</dt> <dd>

Puntero a la etiqueta para la cadena solicitada.

</dd> <dt>

*ppReturnedOwnerName* \[ enuncia\]
</dt> <dd>

Puntero a la variable que apunta a donde se devolverá el nombre del **propietario** .

</dd> <dt>

*ppReturnedCategoryName* \[ enuncia\]
</dt> <dd>

Puntero a la variable que apunta a donde se devolverá el nombre de la **categoría** .

</dd> <dt>

*ppReturnedTagName* \[ enuncia\]
</dt> <dd>

Puntero a la variable que apunta a donde se devolverá el nombre de **etiqueta** .

</dd> <dt>

*ppReturnedString* \[ enuncia\]
</dt> <dd>

Puntero a la variable que apunta a donde se devolverá el nombre de la cadena.

</dd> <dt>

*pRestartKey* \[ enuncia\]
</dt> <dd>

Puntero a la variable donde se especificará y devolverá la clave de reinicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el problema.

Si no existe una combinación especificada de información de **propietario**, **categoría** y **etiqueta** , el valor devuelto es **NMERR la entrada de \_ BLOB no \_ \_ \_ \_ existe**.

Cuando el BLOB se atraviesa completamente dentro de los límites especificados inicialmente, la función devuelve **la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe** y el parámetro *pRestartKey* apunta a cero.

## <a name="remarks"></a>Observaciones

En la llamada inicial a la función **GetStringsFromBlob** , el parámetro *pRestartKey* apunta a una variable que contiene el valor cero. Los parámetros *prequested* solo se pueden usar cuando la clave restart es cero. En las llamadas posteriores, cuando *pRestartKey* tiene valores distintos de cero, se omiten los parámetros *prequested* . En la llamada inicial, All puede señalar a **null**, que configura la consulta para que devuelva todas las entradas del BLOB, una por cada llamada subsiguiente.

Al especificar un propietario, se limitan las cadenas devueltas solo a ese propietario. Se aplica una limitación similar para las categorías y las etiquetas, con la ADVERTENCIA adicional de que, si se especifica una categoría, también se debe especificar un propietario y, si se especifica una etiqueta, se debe especificar una categoría (y, por tanto, un propietario).

Cuando se devuelve la llamada inicial a **GetStringsFromBlob** , *pRestartKey* apunta a un nuevo valor, que se debe especificar en la siguiente llamada a la función para obtener el valor siguiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
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

 

 




