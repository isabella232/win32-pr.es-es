---
description: La función GetFrameSrcAddressOffset devuelve el desplazamiento de la dirección de origen de los fotogramas.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Función GetFrameSrcAddressOffset (Netmon.h)
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
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366099"
---
# <a name="getframesrcaddressoffset-function"></a>Función GetFrameSrcAddressOffset

La **función GetFrameSrcAddressOffset** devuelve el desplazamiento de la dirección de origen del marco.

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

-   TIPO \_ DE \_ DIRECCIÓN ETHERNET
-   DIRECCIÓN \_ IP DE TIPO \_
-   TIPO \_ DE \_ DIRECCIÓN IPX
-   TOKENRING \_ DE TIPO \_ DE DIRECCIÓN
-   TIPO \_ DE \_ DIRECCIÓN FDDI
-   TIPO \_ DE \_ DIRECCIÓN XNS
-   TIPO \_ DE DIRECCIÓN IP DE LA \_ DIRECCION \_
-   ADDRESS \_ TYPE \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Puntero a **un DWORD**, que, a la vuelta, contiene la longitud de la dirección, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el desplazamiento a la dirección de origen.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




