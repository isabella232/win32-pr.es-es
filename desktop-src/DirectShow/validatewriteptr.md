---
description: Comprueba que el proceso de llamada tiene acceso de escritura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Macro ValidateWritePtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e7c955f31cf9e0bf1050c52b680dfc9b32741bb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169878"
---
# <a name="validatewriteptr-macro"></a>ValidateWritePtr (macro)

Comprueba que el proceso de llamada tiene acceso de escritura a un bloque de memoria. Si no es así, la macro llama a la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Esta macro está en desuso. En el SDK Windows para Windows Vista (y versiones posteriores) esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateWritePtr(
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

## <a name="remarks"></a>Observaciones

Esta macro se omite a menos que se defina DEBUG, DEBUG o VFWROBUST cuando se DirectShow archivo de encabezado de \_ clase base. Esta macro puede tener un costo de rendimiento significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




