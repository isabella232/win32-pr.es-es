---
description: La función GetFrameDstAddressOffset devuelve el desplazamiento a la dirección de destino de un fotograma determinado.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Función GetFrameDstAddressOffset (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677281"
---
# <a name="getframedstaddressoffset-function"></a>GetFrameDstAddressOffset función)

La función **GetFrameDstAddressOffset** devuelve el desplazamiento a la dirección de destino de un fotograma determinado.

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

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco.

</dd> <dt>

*AddressType* \[ de\]
</dt> <dd>

Tipo de la dirección de destino. Especifique uno de los valores siguientes:

tipo de dirección Ethernet de tipo dirección IP escriba dirección IP tipo de dirección TOKENRING tipo de dirección FDDI tipo de dirección de XNS tipo de dirección \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IP Vines tipo de dirección \_ IP \_ \_ ATM.

</dd> <dt>

*AddressLength* \[ de\]
</dt> <dd>

Longitud de la dirección de destino, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el desplazamiento (medido en bytes) al tipo de dirección solicitado.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="remarks"></a>Observaciones

Si el parámetro *AddressType* está establecido en el \_ tipo de dirección \_ Ethernet, el valor devuelto de la función **GetFrameDstAddressOffset** siempre es cero. El desplazamiento de una dirección Ethernet siempre es cero.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameDstAddressOffset** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




