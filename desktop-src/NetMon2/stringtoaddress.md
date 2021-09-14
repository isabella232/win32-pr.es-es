---
description: La función StringToAddress convierte una cadena en una dirección.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Función StringToAddress (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245151"
---
# <a name="stringtoaddress-function"></a>Función StringToAddress

La **función StringToAddress** convierte una cadena en una dirección.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpAddress* \[ out\]
</dt> <dd>

Puntero a la dirección a la que se convierte la cadena.

</dd> <dt>

*string* \[ En\]
</dt> <dd>

Cadena que se convierte en una dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un puntero a la cadena convertida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




