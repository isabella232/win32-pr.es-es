---
description: Comprueba que el proceso de llamada tiene acceso de lectura a una cadena. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691035"
---
# <a name="validatestringptr-macro"></a>ValidateStringPtr (macro)

Comprueba que el proceso de llamada tiene acceso de lectura a una cadena. Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro está en desuso. En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.

 

## <a name="syntax"></a>Sintaxis


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Puntero a una cadena de **TCHAR** terminada en NULL.

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

 

 




