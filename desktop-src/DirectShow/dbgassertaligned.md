---
description: Comprueba si un puntero está alineado con un límite especificado. Si no es así, esta macro invoca la macro ASSERT. Se omite en las compilaciones comerciales.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 36b835ccd7fd82e226eb76dfb45ca4cfcd034a713da0d3639e91fba8aa7e4fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953354"
---
# <a name="dbgassertaligned-macro"></a>Macro DbgAssertAligned

Comprueba si un puntero está alineado con un límite especificado. Si no es así, esta macro invoca la macro [**ASSERT.**](assert.md) Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ptr* 
</dt> <dd>

Variable de puntero.

</dd> <dt>

*Alineación* 
</dt> <dd>

Alineación necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




