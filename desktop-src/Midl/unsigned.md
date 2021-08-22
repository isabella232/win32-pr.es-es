---
title: atributo unsigned
description: La palabra clave unsigned indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- midl de atributo sin signo
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 383a8fc0379ca81abb9ad0a88edab8750661bdfa429e32e7e91d193aa0fd2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146178"
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

## <a name="remarks"></a>Comentarios

Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de caracteres y enteros [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)y [**small**](small.md). Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **long**, **short** y **small**.

Cuando se usa el modificador del compilador MIDL [**/char**](-char.md), los tipos de caracteres y enteros que aparecen en el archivo IDL sin palabras clave sign explícitas pueden aparecer con la palabra clave [**signed**](signed.md) o **unsigned** en el archivo de encabezado generado. Para evitar confusiones, especifique el signo de los tipos de entero y carácter.

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

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




