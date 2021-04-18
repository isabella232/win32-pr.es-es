---
description: Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691036"
---
# <a name="validatereadptr-macro"></a>ValidateReadPtr (macro)

Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria. Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro está en desuso. En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Puntero a un bloque de memoria.

</dd> <dt>

*CB* 
</dt> <dd>

Tamaño del bloque de memoria, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta macro se omite a menos que se defina DEBUG, \_ Debug o VFWROBUST cuando se incluye el archivo de encabezado de clase base de DirectShow. Esta macro puede tener un costo de rendimiento considerable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




