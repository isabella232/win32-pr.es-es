---
description: La función AddressToString convierte una dirección en una cadena.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Función AddressToString (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 58c105fb8fa646fbffcc7d7d4a3f1dad3a9cd86e7bb6ef8cc426dc982873f720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796375"
---
# <a name="addresstostring-function"></a>Función AddressToString

La **función AddressToString** convierte una dirección en una cadena.

## <a name="syntax"></a>Sintaxis


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cadena* \[ out\]
</dt> <dd>

Cadena a la que se convierte la dirección.

</dd> <dt>

*lpAddress* \[ En\]
</dt> <dd>

Dirección que se imprime.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un puntero a la cadena convertida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




