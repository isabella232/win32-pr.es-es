---
description: La función GetNetworkInfoFromBlob recupera información de red de un BLOB determinado.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Función GetNetworkInfoFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678584"
---
# <a name="getnetworkinfofromblob-function"></a>GetNetworkInfoFromBlob función)

La función **GetNetworkInfoFromBlob** recupera información de red de un BLOB determinado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador de un BLOB.

</dd> <dt>

*lpNetworkInfo* \[ in, out\]
</dt> <dd>

Puntero a la estructura [NETWORKINFO](networkinfo.md) asignada por el usuario que se rellena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función **GetNetworkInfoFromBlob** se ejecuta correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.

## <a name="remarks"></a>Observaciones

La información de red se almacena en la sección BLOB **NetworkInfo** de la categoría de **propietario** de BLOB NPP.

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

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
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

 

 




