---
description: La función GetDwordFromBlob recupera el valor DWORD con nombre de un BLOB.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: Función GetDwordFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153857"
---
# <a name="getdwordfromblob-function"></a>GetDwordFromBlob función)

La función **GetDwordFromBlob** recupera el valor **DWORD** con nombre de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador de un BLOB.

</dd> <dt>

*pOwnerName* \[ de\]
</dt> <dd>

Puntero al nombre del propietario del BLOB.

</dd> <dt>

*pCategoryName* \[ de\]
</dt> <dd>

Puntero al nombre de la categoría de BLOB.

</dd> <dt>

*pTagName* \[ de\]
</dt> <dd>

Puntero al nombre de la etiqueta de BLOB.

</dd> <dt>

*pDword* \[ enuncia\]
</dt> <dd>

Puntero al valor **DWORD** del BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.

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

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
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

 

 




