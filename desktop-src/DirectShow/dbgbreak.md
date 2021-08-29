---
description: Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de origen y el número de línea. El usuario puede omitir el mensaje, escribir el depurador o salir de la aplicación. Se omite en las compilaciones comerciales.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: bb727a573efebc2957d5eaddfb32d077d981503fb7bd8a7c9481e6841dcd901a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052045"
---
# <a name="dbgbreak-macro"></a>Macro DbgBreak

Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de origen y el número de línea. El usuario puede omitir el mensaje, escribir el depurador o salir de la aplicación. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strLiteral* 
</dt> <dd>

Cadena de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve un valor.

## <a name="examples"></a>Ejemplos


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




