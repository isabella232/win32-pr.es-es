---
description: La función CCHeapAlloc asigna memoria en función de la captura.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Función CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909417"
---
# <a name="ccheapalloc-function"></a>CCHeapAlloc función)

La función **CCHeapAlloc** asigna memoria en función de la captura.

## <a name="syntax"></a>Sintaxis


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwBytes* 
</dt> <dd>

Longitud de memoria solicitada asignada.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indicador de si se inicializó la memoria asignada. Si el valor del parámetro es **true**, la memoria asignada se inicializa en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada. Cuando haya terminado de usar la memoria asignada, libere la memoria mediante una llamada a la función [**CCHeapFree**](ccheapfree.md) .

Si la función no se realiza correctamente, el valor devuelto es **null**.

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

[**SetCCInstPtr**](setccinstptr.md)
</dt> <dt>

[**GetCCInstPtr**](getccinstptr.md)
</dt> <dt>

[**CCHeapFree**](ccheapfree.md)
</dt> <dt>

[**CCHeapReAlloc**](ccheaprealloc.md)
</dt> <dt>

[**CCHeapSize**](ccheapsize.md)
</dt> </dl>

 

 




