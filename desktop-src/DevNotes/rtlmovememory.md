---
description: Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite bloques de memoria de origen y de destino superpuestos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Función RtlMoveMemory (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: bf4366633de321e27f6d3cdc0396fcdce81b0dac30b0d09a4c2c4675706d939e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161667"
---
# <a name="rtlmovememory-function"></a>Función RtlMoveMemory

Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite bloques de memoria de origen y de destino superpuestos.

## <a name="syntax"></a>Sintaxis


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* \[ out\]
</dt> <dd>

Puntero al bloque de memoria de destino en el que se copian los bytes.

</dd> <dt>

*Origen* \[ En\]
</dt> <dd>

Puntero al bloque de memoria de origen del que se copian los bytes.

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Número de bytes que se copian del origen al destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno

## <a name="remarks"></a>Observaciones

El bloque de memoria de origen, definido por *Source* y *Length*, puede superponerse al bloque de memoria de destino, definido por *Destination* y *Length*.

La [**rutina RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) se ejecuta más rápido que **RtlMoveMemory,** pero **RtlCopyMemory** requiere que los bloques de memoria de origen y destino no se superpongan.

Los llamadores **de RtlMoveMemory** pueden ejecutarse en cualquier IRQL si los bloques de memoria de origen y destino están en memoria del sistema sin página. De lo contrario, el autor de la llamada debe ejecutarse en IRQL <= APC \_ LEVEL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Wdm.h (incluya Wdm.h, Ntddk.h o Ntifs.h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
