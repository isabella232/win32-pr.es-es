---
description: La función CompareAddresses compara dos direcciones, lo que indica que una de las direcciones es mayor, menor o igual que la otra dirección.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Función CompareAddresses (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253880"
---
# <a name="compareaddresses-function"></a>Función CompareAddresses

La **función CompareAddresses** compara dos direcciones, lo que indica que una de las direcciones es mayor, menor o igual que la otra dirección.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpAddress1* \[ En\]
</dt> <dd>

Puntero a la primera dirección.

</dd> <dt>

*lpAddress2* \[ En\]
</dt> <dd>

Puntero a la segunda dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si las direcciones son las mismas, la función devuelve cero.

Si el *parámetro lpAddress1* especifica una dirección que es menor que la dirección especificada por el parámetro *lpAddress2,* el valor devuelto es un número negativo.

Si el *parámetro lpAddress1* especifica una dirección mayor que la dirección especificada por el parámetro *lpAddress2,* el valor devuelto es un número positivo.

## <a name="remarks"></a>Observaciones

Una dirección que es menor que otra dirección indica un marco anterior. Una dirección mayor que otra dirección indica un marco posterior.

Monitor de red proporciona otras dos funciones, [CompareFrameDestAddress](compareframedestaddress.md) y [CompareFrameSourceAddress,](compareframesourceaddress.md)que puede usar para comparar direcciones. La **función CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la **función CompareFrameSourceAddress** compara una dirección determinada con la dirección de origen del marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




