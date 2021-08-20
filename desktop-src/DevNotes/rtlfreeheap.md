---
description: Libera un bloque de memoria asignado desde un montón por RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Función RtlFreeHeap (Ntifs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538084"
---
# <a name="rtlfreeheap-function"></a>Función RtlFreeHeap

Libera un bloque de memoria asignado desde un montón por [**RtlAllocateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)

## <a name="syntax"></a>Sintaxis


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HeapHandle* \[ En\]
</dt> <dd>

Identificador del montón cuyo bloque de memoria se va a liberar. Este parámetro es un identificador devuelto por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).

</dd> <dt>

*Marcas* \[ in, opcional\]
</dt> <dd>

Conjunto de marcas que controla aspectos de liberar un bloque de memoria. Al especificar el siguiente valor, se invalida el valor correspondiente que se especificó en el *parámetro Flags* cuando [**rtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)creó el montón.



| Marca                           | Significado                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| MONTÓN \_ SIN \_ SERIALIZACIÓN<br/> | La exclusión mutua no se usará **cuando RtlFreeHeap** acceda al montón. <br/> |



 

</dd> <dt>

*HeapBase* \[ En\]
</dt> <dd>

Puntero al bloque de memoria que se liberará. [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)devuelve este puntero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el bloque se ha liberado correctamente; **False en** caso contrario.

> [!Note]  
> A partir Windows 8 el valor devuelto se escribe **como LOGICAL**, que tiene un tamaño diferente al **booleano**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntifs.h (incluir Ntifs.h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
