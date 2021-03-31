---
description: La función HTMLValueToUnicode convierte una \_ cadena UTF8 de CP HTML en una cadena Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Función HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808701"
---
# <a name="htmlvaluetounicode-function"></a>HTMLValueToUnicode función)

La función **HTMLValueToUnicode** convierte una \_ cadena UTF8 de CP HTML en una cadena Unicode.

## <a name="syntax"></a>Sintaxis


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* \[ in, out\]
</dt> <dd>

En la entrada, puntero a la cadena HTML proporcionada por MCSVC.

En la salida, puntero a la cadena Unicode convertida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el equivalente Unicode de la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




