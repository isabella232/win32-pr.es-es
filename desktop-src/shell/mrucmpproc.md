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
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256965"
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

## <a name="remarks"></a>Observaciones

Esta función se puede especificar opcionalmente para su uso en la estructura [**MRUINFO**](mruinfo.md) pasada a [**CreateMRUListW**](createmrulist.md). Esto resulta útil cuando se creó la lista de MRU con la **marca \_ BINARY de MRU.** Cuando no se especifica esta función, se usan funciones de comparación de cadenas estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>            |
| Nombres Unicode y ANSI<br/>   | **MRUCMPPROCW** (Unicode) y **MRUCMPPROCA** (ANSI)<br/> |



 

 




