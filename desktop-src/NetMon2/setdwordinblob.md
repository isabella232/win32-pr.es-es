---
description: La función SetDwordInBlob establece el valor DWORD con nombre de un BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Función SetDwordInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0fdc05052542c8606bf72d7250e29086a59b6cc69761229df4800abdc781027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364053"
---
# <a name="setdwordinblob-function"></a>Función SetDwordInBlob

La **función SetDwordInBlob** establece el valor **DWORD** con nombre de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador de un BLOB que se está configurando.

</dd> <dt>

*pOwnerName* \[ En\]
</dt> <dd>

Puntero al nombre del **propietario de** BLOB que se va a establecer.

</dd> <dt>

*pCategoryName* \[ En\]
</dt> <dd>

Puntero al nombre de **la categoría** BLOB que se va a establecer.

</dd> <dt>

*pTagName* \[ En\]
</dt> <dd>

Puntero al nombre de **la etiqueta** BLOB que se va a establecer.

</dd> <dt>

*Dword* \[ En\]
</dt> <dd>

**Valor DWORD** del BLOB que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el error.

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

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
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
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




