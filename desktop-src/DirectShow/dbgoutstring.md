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
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821571"
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

## <a name="remarks"></a>Comentarios

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

 

 




