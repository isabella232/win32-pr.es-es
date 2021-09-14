---
description: La función GetFrameDstAddressOffset devuelve el desplazamiento a la dirección de destino de un fotograma determinado.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Función GetFrameDstAddressOffset (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169306"
---
# <a name="getframedstaddressoffset-function"></a>Función GetFrameDstAddressOffset

La **función GetFrameDstAddressOffset** devuelve el desplazamiento a la dirección de destino de un fotograma determinado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco.

</dd> <dt>

*AddressType* \[ En\]
</dt> <dd>

Tipo de la dirección de destino. Especifique uno de los valores siguientes:

TIPO DE DIRECCIÓN TIPO DE DIRECCIÓN ETHERNET TIPO DE DIRECCIÓN IP TIPO DE DIRECCIÓN \_ \_ IPX TOKENRING ADDRESS \_ TYPE \_ \_ \_ \_ \_ \_ \_ FDDI ADDRESS TYPE \_ \_ XNS ADDRESS \_ TYPE \_ HEXADECIMALS IP ADDRESS TYPE \_ \_ \_ ATM.

</dd> <dt>

*AddressLength* \[ En\]
</dt> <dd>

Longitud de la dirección de destino, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el desplazamiento (medido en bytes) al tipo de dirección solicitado.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="remarks"></a>Observaciones

Si el *parámetro AddressType* se establece en ADDRESS TYPE ETHERNET, el valor devuelto de la función \_ \_ **GetFrameDstAddressOffset** siempre es cero. El desplazamiento de una dirección Ethernet siempre es cero.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetFrameDstAddressOffset.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




