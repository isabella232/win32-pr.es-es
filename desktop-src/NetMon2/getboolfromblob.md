---
description: Recupera un valor booleano con nombre de un BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Función GetBoolFromBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: ec9f5333e3f85f92b30d52689288c971ca04437df647a7a7e5fe89379e06533e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743925"
---
# <a name="getboolfromblob-function"></a>Función GetBoolFromBlob

La **función GetBoolFromBlob** recupera un valor booleano con nombre de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador de un BLOB.

</dd> <dt>

*pOwnerName* \[ En\]
</dt> <dd>

Puntero al nombre del propietario de BLOB.

</dd> <dt>

*pCategoryName* \[ En\]
</dt> <dd>

Puntero al nombre de categoría BLOB.

</dd> <dt>

*pTagName* \[ En\]
</dt> <dd>

Puntero al nombre de la etiqueta BLOB.

</dd> <dt>

*pBool* \[ out\]
</dt> <dd>

Puntero al valor booleano del BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que describe el error.

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

[SetBoolInBlob](setboolinblob.md)
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
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




