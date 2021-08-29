---
description: La función CompareFrameSourceAddress compara una dirección con la dirección de origen de un marco.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Función CompareFrameSourceAddress (Netmon.h)
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
ms.openlocfilehash: 8738f1322f30baeb5152f5f453cc8d77c74405889caaf667a3d73413d9cdad96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891105"
---
# <a name="compareframesourceaddress-function"></a>Función CompareFrameSourceAddress

La **función CompareFrameSourceAddress** compara una dirección con la dirección de origen de un marco.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador de un marco.

</dd> <dt>

*lpAddress* \[ En\]
</dt> <dd>

Puntero a una dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si las direcciones son las mismas, el valor devuelto es **TRUE.**

Si las direcciones no son las mismas, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Para que **la función CompareFrameSourceAddress** se haga correctamente, el tipo de dirección de origen debe coincidir con el tipo de dirección especificado en el *parámetro lpAddress.*

Monitor de red proporciona otras dos funciones para comparar direcciones: [CompareFrameDestAddress](compareframedestaddress.md) y [CompareAddresses](compareaddresses.md). La **función CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la **función CompareAddress** compara dos direcciones determinadas.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función CompareFrameSourceAddress.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




