---
description: Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).
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
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001338"
---
# <a name="mrucmpproc-callback-function"></a>Función de devolución de llamada MRUCMPPROC

Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).

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

Segunda cadena que se va a comparar con la primera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve 0 si los elementos son idénticos, un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Observaciones

Esta función se puede especificar opcionalmente para su uso en la estructura [**MRUINFO**](mruinfo.md) pasada a [**CreateMRUListW**](createmrulist.md). Esto resulta útil cuando la lista MRU se creó con la **marca \_ binaria MRU** . Cuando no se especifica esta función, se usan las funciones de comparación de cadenas estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>            |
| Nombres Unicode y ANSI<br/>   | **MRUCMPPROCW** (Unicode) y **MRUCMPPROCA** (ANSI)<br/> |



 

 




