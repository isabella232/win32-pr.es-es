---
description: La función MacTypeToAddressType convierte un tipo MAC determinado en un tipo de dirección.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Función MacTypeToAddressType (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908095"
---
# <a name="mactypetoaddresstype-function"></a>MacTypeToAddressType función)

La función **MacTypeToAddressType** convierte un tipo Mac determinado en un tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MacType* \[ de\]
</dt> <dd>

Tipo MAC que se va a convertir. Especifique uno de los valores siguientes:

tipo \_ Mac \_ Ethernet Mac \_ tipo \_ TOKENRING Mac \_ tipo \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de direcciones.

tipo de dirección \_ \_ Ethernet Dirección tipo \_ \_ TOKENRING \_ tipo de dirección \_ FDDI

Si la función no es correcta, el tipo MAC es desconocido, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **MacTypeToAddressType** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




