---
description: Comprueba que el proceso de llamada tiene acceso de lectura y escritura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ec4d1c0440d0747024efadaa441ca062da512283f5a01f29be12b19c0f7c0567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755665"
---
# <a name="validatereadwriteptr-macro"></a>ValidateReadWritePtr (macro)

Comprueba que el proceso de llamada tiene acceso de lectura y escritura a un bloque de memoria. Si no es así, la macro llama a la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Esta macro está en desuso. En el SDK Windows para Windows Vista (y versiones posteriores) esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p* 
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

Esta macro se omite a menos que se defina DEBUG, DEBUG o VFWROBUST cuando se DirectShow archivo de encabezado \_ de clase base. Esta macro puede tener un costo de rendimiento significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




