---
description: La función CompareFrameDestAddress compara una dirección con la dirección de destino de un marco.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Función CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909414"
---
# <a name="compareframedestaddress-function"></a>CompareFrameDestAddress función)

La función **CompareFrameDestAddress** compara una dirección con la dirección de destino de un marco.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador de un marco.

</dd> <dt>

*lpAddress* \[ de\]
</dt> <dd>

Puntero a una dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si las direcciones son las mismas, el valor devuelto es **true**.

Si las direcciones no son iguales, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Para que la función **CompareFrameDestAddress** se devuelva correctamente, el tipo de dirección de destino debe coincidir con el tipo de dirección especificado en el parámetro *lpAddress* .

Monitor de red proporciona otras dos funciones, [CompareFrameSourceAddress](compareframesourceaddress.md) y [CompareAddresses](compareaddresses.md), que puede usar para comparar direcciones. La función **CompareFrameSourceAddress** compara una dirección determinada con la dirección de origen del marco y la función **CompareAddress** compara dos direcciones dadas.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **CompareFrameDestAddress** .

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

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




