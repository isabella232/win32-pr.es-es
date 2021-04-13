---
description: La función CompareFrameSourceAddress compara una dirección con la dirección de origen de un marco.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Función CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278145"
---
# <a name="compareframesourceaddress-function"></a>CompareFrameSourceAddress función)

La función **CompareFrameSourceAddress** compara una dirección con la dirección de origen de un marco.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CompareFrameSourceAddress(
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

Para que la función **CompareFrameSourceAddress** se ejecute correctamente, el tipo de dirección de origen debe coincidir con el tipo de dirección especificado en el parámetro *lpAddress* .

Monitor de red proporciona otras dos funciones para comparar direcciones: [CompareFrameDestAddress](compareframedestaddress.md) y [CompareAddresses](compareaddresses.md). La función **CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la función **CompareAddress** compara dos direcciones dadas.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **CompareFrameSourceAddress** .

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




