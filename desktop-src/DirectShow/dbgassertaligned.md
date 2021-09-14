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
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362446"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




