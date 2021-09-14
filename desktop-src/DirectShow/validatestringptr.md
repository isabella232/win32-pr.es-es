---
description: Comprueba que el proceso de llamada tiene acceso de lectura a una cadena. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug.h)
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
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169889"
---
# <a name="validatestringptr-macro"></a>ValidateStringPtr (macro)

Comprueba que el proceso de llamada tiene acceso de lectura a una cadena. Si no es así, la macro llama a la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Esta macro está en desuso. En el SDK Windows para Windows Vista (y versiones posteriores) esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*P* 
</dt> <dd>

Puntero a una cadena **TCHAR terminada en** NULL.

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

 

 




