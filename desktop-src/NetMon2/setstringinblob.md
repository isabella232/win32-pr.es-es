---
description: Establece una cadena en una ubicación determinada dentro de un BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Función SetStringInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363684"
---
# <a name="setstringinblob-function"></a>Función SetStringInBlob

La **función SetStringInBlob** establece una cadena en una ubicación determinada dentro de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*pOwnerName* \[ En\]
</dt> <dd>

Puntero a la **sección Propietario** del BLOB, donde se establece la cadena.

</dd> <dt>

*pCategoryName* \[ En\]
</dt> <dd>

Puntero a la **sección Category** del BLOB, donde se establece la cadena.

</dd> <dt>

*pTagName* \[ En\]
</dt> <dd>

Puntero a la **etiqueta de** la cadena solicitada.

</dd> <dt>

*pString* \[ En\]
</dt> <dd>

Puntero a la variable donde se devolverá un puntero a la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el problema.

Si la información **de propietario,** **categoría** o etiqueta especificada no existe, el valor devuelto es NMERR BLOB ENTRY DOES NOT  \_ \_ \_ \_ \_ EXIST.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> </dl>

 

 




