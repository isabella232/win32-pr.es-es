---
description: Libera el identificador asociado a la lista de elementos usados más recientemente (MRU) y escribe los datos almacenados en caché en el registro.
title: FreeMRUList función)
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985486"
---
# <a name="freemrulist-function"></a>FreeMRUList función)

Libera el identificador asociado a la lista de elementos usados más recientemente (MRU) y escribe los datos almacenados en caché en el registro.

## <a name="syntax"></a>Sintaxis


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMRU* \[ de\]
</dt> <dd>

Tipo: **Handle**

Identificador de la lista MRU que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un valor no negativo si es correcto; de lo contrario,-1.

## <a name="remarks"></a>Observaciones

Si la lista MRU se creó con la **marca \_ CACHEWRITE MRU** , al llamar a **FreeMRUList** , los cambios que todavía no se hayan escrito en la versión de la lista MRU almacenada en el registro se escribirán en este momento.

Esta función no está incluida en un encabezado público o una biblioteca. Debe extraerse de comctl32.dll por el ordinal 152.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 




