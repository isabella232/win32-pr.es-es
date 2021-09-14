---
description: La función MacTypeToAddressType convierte un tipo MAC determinado en un tipo de dirección.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Función MacTypeToAddressType (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245355"
---
# <a name="mactypetoaddresstype-function"></a>Función MacTypeToAddressType

La **función MacTypeToAddressType** convierte un tipo MAC determinado en un tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MacType* \[ En\]
</dt> <dd>

Tipo de MAC que se va a convertir. Especifique uno de los valores siguientes:

MAC \_ TYPE \_ ETHERNET MAC \_ TYPE \_ TOKENRING MAC \_ TYPE \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de direcciones.

TIPO \_ DE DIRECCIÓN ETHERNET TIPO DE DIRECCIÓN \_ \_ \_ TOKENRING ADDRESS TYPE \_ \_ FDDI

Si la función no se realiza correctamente, se desconoce el tipo MAC, el valor devuelto es -1.

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función MacTypeToAddressType.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




