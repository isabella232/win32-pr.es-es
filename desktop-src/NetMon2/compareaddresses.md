---
description: La función CompareAddresses compara dos direcciones, lo que indica que una de las direcciones es mayor que, menor o igual que la otra dirección.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Función CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667736"
---
# <a name="compareaddresses-function"></a>CompareAddresses función)

La función **CompareAddresses** compara dos direcciones, lo que indica que una de las direcciones es mayor que, menor o igual que la otra dirección.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpAddress1* \[ de\]
</dt> <dd>

Puntero a la primera dirección.

</dd> <dt>

*lpAddress2* \[ de\]
</dt> <dd>

Puntero a la segunda dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si las direcciones son iguales, la función devuelve cero.

Si el parámetro *lpAddress1* especifica una dirección que es menor que la dirección que especifica el parámetro *lpAddress2* , el valor devuelto es un número negativo.

Si el parámetro *lpAddress1* especifica una dirección que es mayor que la dirección que especifica el parámetro *lpAddress2* , el valor devuelto es un número positivo.

## <a name="remarks"></a>Observaciones

Una dirección que es menor que otra dirección indica un fotograma anterior. Una dirección que es mayor que otra dirección indica un fotograma posterior.

Monitor de red proporciona otras dos funciones, [CompareFrameDestAddress](compareframedestaddress.md) y [CompareFrameSourceAddress](compareframesourceaddress.md), que puede usar para comparar direcciones. La función **CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la función **CompareFrameSourceAddress** compara una dirección determinada con la dirección de origen del marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




