---
description: Se usa para determinar si un elemento está presente en una lista usada más recientemente (MRU).
title: Función de devolución de llamada MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: bcf8bb7c8ec4ceab299efd75c61cabe86f43d0ee46585be59ab4000957554ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111495"
---
# <a name="mrucmpproc-callback-function"></a>Función de devolución de llamada MRUCMPPROC

Se usa para determinar si un elemento está presente en una lista usada más recientemente (MRU).

## <a name="syntax"></a>Sintaxis


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pString1* 
</dt> <dd>

Tipo: **LPCTSTR**

La primera cadena.

</dd> <dt>

*pString2* 
</dt> <dd>

Tipo: **LPCTSTR**

Segunda cadena que se comparará con la primera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve 0 si los elementos son idénticos; de lo contrario, un valor distinto de cero.

## <a name="remarks"></a>Comentarios

Esta función se puede especificar opcionalmente para su uso en la estructura [**MRUINFO**](mruinfo.md) pasada a [**CreateMRUListW**](createmrulist.md). Esto resulta útil cuando se creó la lista de MRU con la **marca \_ BINARY de MRU.** Cuando no se especifica esta función, se usan funciones de comparación de cadenas estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>            |
| Nombres Unicode y ANSI<br/>   | **MRUCMPPROCW** (Unicode) y **MRUCMPPROCA** (ANSI)<br/> |



 

 




