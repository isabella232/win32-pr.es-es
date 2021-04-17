---
description: Comprueba si un puntero está alineado con un límite especificado. En caso contrario, esta macro invoca la macro Assert. Se omite en las compilaciones comerciales.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681058"
---
# <a name="dbgassertaligned-macro"></a>DbgAssertAligned (macro)

Comprueba si un puntero está alineado con un límite especificado. En caso contrario, esta macro invoca la macro [**Assert**](assert.md) . Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptr* 
</dt> <dd>

Variable de puntero.

</dd> <dt>

*ecuación* 
</dt> <dd>

Alineación requerida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros Assert y Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




