---
description: La función CCHeapReAlloc reasigna la memoria asignada por la función CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Función CCHeapReAlloc (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0679b80531c679beaee9eaf56be24ae16f6abea566b74d1928d4fa31fbf37747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144338"
---
# <a name="ccheaprealloc-function"></a>Función CCHeapReAlloc

La **función CCHeapReAlloc** reasigna la memoria asignada por la **función CCHeapAlloc.**

## <a name="syntax"></a>Sintaxis


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpMem* 
</dt> <dd>

Puntero a la memoria asignada original.

</dd> <dt>

*dwBytes* 
</dt> <dd>

Tamaño de la memoria reasignada, medida en bytes.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indicador de si se inicializó la memoria reasignada. Si el valor del parámetro **es TRUE,** la memoria recién reasignada se inicializa en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria reasignada.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

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

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




