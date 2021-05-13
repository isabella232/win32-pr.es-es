---
description: Libera el identificador asociado a la lista de MRU usada más recientemente y escribe los datos almacenados en caché en el registro.
title: Función FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840626"
---
# <a name="freemrulist-function"></a>Función FreeMRUList

Libera el identificador asociado a la lista de MRU usada más recientemente y escribe los datos almacenados en caché en el registro.

## <a name="syntax"></a>Sintaxis


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMRU* \[ En\]
</dt> <dd>

Tipo: **HANDLE**

Identificador de la lista de MRU que se liberará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un valor no negativo si se realiza correctamente; de lo contrario, -1.

## <a name="remarks"></a>Observaciones

Si la lista de MRU se creó con la marca **\_ MRU CACHEWRITE,** llamar a **FreeMRUList** hace que los cambios que aún no se han escrito en la versión de la lista de MRU almacenada en el Registro se escriban en este momento.

Esta función no se incluye en un encabezado o biblioteca públicos. Debe extraerse de comctl32.dll mediante el ordinal 152.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 




