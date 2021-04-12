---
description: La función GetFrameSrcAddressOffset devuelve el desplazamiento de la dirección de origen de los marcos.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Función GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277979"
---
# <a name="getframesrcaddressoffset-function"></a>GetFrameSrcAddressOffset función)

La función **GetFrameSrcAddressOffset** devuelve el desplazamiento de la dirección de origen del marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Identificador del marco.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo de dirección de origen. El valor del parámetro puede ser uno de los siguientes:

-   tipo de dirección \_ \_ Ethernet
-   tipo de dirección \_ \_ IP
-   tipo de dirección \_ \_ IPX
-   tipo de dirección \_ \_ TOKENRING
-   tipo de dirección \_ \_ FDDI
-   tipo de dirección \_ \_ XNS
-   tipo de dirección \_ \_ IP Vines \_
-   tipo de dirección \_ \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Puntero a un **valor DWORD**, que, en la devolución, contiene la longitud de la dirección, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el desplazamiento de la dirección de origen.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




