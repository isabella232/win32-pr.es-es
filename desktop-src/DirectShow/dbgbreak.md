---
description: Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea. El usuario puede omitir el mensaje, entrar en el depurador o salir de la aplicación. Se omite en las compilaciones comerciales.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
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
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661243"
---
# <a name="dbgbreak-macro"></a>DbgBreak (macro)

Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea. El usuario puede omitir el mensaje, entrar en el depurador o salir de la aplicación. Se omite en las compilaciones comerciales.

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

Esta macro no devuelve ningún valor.

## <a name="examples"></a>Ejemplos


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros Assert y Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




