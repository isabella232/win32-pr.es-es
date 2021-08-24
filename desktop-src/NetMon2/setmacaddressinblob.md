---
description: La función SetMacAddressInBlob establece la dirección MAC solicitada de un BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Función SetMacAddressInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 20ed4a0358bc0aecada66858f9814bce94252ff9d705c971be947ca5af788ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364063"
---
# <a name="setmacaddressinblob-function"></a>Función SetMacAddressInBlob

La **función SetMacAddressInBlob** establece la dirección MAC solicitada de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Controle el BLOB que se va a establecer.

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

*pMacAddress* \[ En\]
</dt> <dd>

Puntero a la dirección MAC del BLOB que se va a establecer.

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

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
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

 

 




