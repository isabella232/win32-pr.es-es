---
description: Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug.h)
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
ms.openlocfilehash: caf429437d284a27e4cda830b51e4512375310f2d466a597e58c394a2fea551f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501635"
---
# <a name="validatereadptr-macro"></a>Macro ValidateReadPtr

Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria. Si no es así, la macro llama a la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Esta macro está en desuso. En el SDK Windows para Windows Vista (y versiones posteriores), esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*P* 
</dt> <dd>

Puntero a un bloque de memoria.

</dd> <dt>

*Cb* 
</dt> <dd>

Tamaño del bloque de memoria, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve un valor.

## <a name="remarks"></a>Comentarios

Esta macro se omite a menos que se defina DEBUG, DEBUG o VFWROBUST cuando se DirectShow archivo de encabezado de \_ clase base. Esta macro puede tener un costo de rendimiento significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




