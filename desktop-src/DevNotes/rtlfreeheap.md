---
description: Libera un bloque de memoria que se ha asignado desde un montón mediante RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Función RtlFreeHeap (Ntifs. h)
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
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538842"
---
# <a name="rtlfreeheap-function"></a>RtlFreeHeap función)

Libera un bloque de memoria que se ha asignado desde un montón mediante [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

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

*HeapHandle* \[ de\]
</dt> <dd>

Identificador del montón cuyo bloque de memoria se va a liberar. Este parámetro es un identificador devuelto por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).

</dd> <dt>

*Marcas* \[ de en, opcional\]
</dt> <dd>

Conjunto de marcas que controla aspectos de liberar un bloque de memoria. Si se especifica el valor siguiente, se invalida el valor correspondiente que se especificó en el parámetro *Flags* cuando [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)creó el montón.



| Marca                           | Significado                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| MONTÓN \_ no \_ SERIALIZE<br/> | La exclusión mutua no se utilizará cuando **RtlFreeHeap** tenga acceso al montón. <br/> |



 

</dd> <dt>

*HeapBase* \[ de\]
</dt> <dd>

Puntero al bloque de memoria que se va a liberar. [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)devuelve este puntero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el bloque se liberó correctamente; De lo contrario, **false** .

> [!Note]  
> A partir de Windows 8, el valor devuelto se escribe como **lógico**, que tiene un tamaño diferente que el **booleano**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Encabezado<br/>                   | <dl> <dt>Ntifs. h (incluye Ntifs. h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
