---
title: atributo unsigned
description: La palabra clave unsigned indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- MIDL de atributo sin signo
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159331"
---
# <a name="unsigned-attribute"></a>atributo unsigned

La **palabra clave unsigned** indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Puede ser cualquiera de [**char,**](char-idl.md) [**wchar \_ t,**](wchar-t.md) [**long,**](long.md) [**int,**](int.md) [**short**](short.md)y [**small.**](small.md)

</dd> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de caracteres y enteros [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long,**](long.md) [**short**](short.md)y [**small**](small.md). Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **long**, **short** y **small.**

Cuando se usa el modificador del compilador MIDL [**/char**](-char.md), los tipos de caracteres y enteros que aparecen en el archivo IDL sin palabras clave de signo explícitas pueden aparecer con la palabra clave [**signed**](signed.md) o **unsigned** en el archivo de encabezado generado. Para evitar confusiones, especifique el signo de los tipos enteros y de caracteres.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**Largo**](long.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




