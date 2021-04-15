---
description: Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite los bloques de memoria de origen y de destino superpuestos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Función RtlMoveMemory (WDM. h)
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
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666176"
---
# <a name="rtlmovememory-function"></a>RtlMoveMemory función)

Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite los bloques de memoria de origen y de destino superpuestos.

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

*Destino* \[ de enuncia\]
</dt> <dd>

Puntero al bloque de memoria de destino en el que se van a copiar los bytes.

</dd> <dt>

*Origen* \[ de de\]
</dt> <dd>

Puntero al bloque de memoria de origen desde el que se van a copiar los bytes.

</dd> <dt>

*Longitud* \[ de\]
</dt> <dd>

Número de bytes que se van a copiar desde el origen al destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

None

## <a name="remarks"></a>Observaciones

El bloque de memoria de origen, que se define mediante el *origen* y la *longitud*, puede superponer el bloque de memoria de destino, que se define mediante el *destino* y la *longitud*.

La rutina [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) se ejecuta más rápido que **RtlMoveMemory**, pero **RtlCopyMemory** requiere que los bloques de memoria de origen y de destino no se superpongan.

Los autores de llamadas de **RtlMoveMemory** se pueden ejecutar en cualquier IRQL si los bloques de memoria de origen y de destino están en la memoria no paginada del sistema. De lo contrario, el llamador debe ejecutarse en IRQL <= \_ nivel APC.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Encabezado<br/>                   | <dl> <dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
