---
description: La función DbgOutString envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Función DbgOutString (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063278"
---
# <a name="dbgoutstring-function"></a>Función DbgOutString

La **función DbgOutString** envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psz* 
</dt> <dd>

Cadena que se genera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En las compilaciones de depuración, esta función siempre genera la cadena, independientemente de los niveles de salida de depuración actuales. Para un control más preciso sobre la salida, use la [**macro DbgLog.**](dbglog.md)

## <a name="examples"></a>Ejemplos


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




