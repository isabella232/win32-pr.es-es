---
title: unsigned (atributo)
description: La palabra clave unsigned indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- atributo sin signo MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665759"
---
# <a name="unsigned-attribute"></a>unsigned (atributo)

La palabra clave **unsigned** indica que el bit más significativo de una variable de entero representa un bit de datos en lugar de un bit con signo.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Puede ser cualquiera de [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)y [**Small**](small.md).

</dd> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de carácter y entero [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md). Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **Long**, **Short** y **Small**.

Cuando se usa el modificador de compilador MIDL [**/Char**](-char.md), los tipos de carácter y entero que aparecen en el archivo IDL sin palabras clave explícitas de signo pueden aparecer con la palabra clave [**signed**](signed.md) o **unsigned** en el archivo de encabezado generado. Para evitar confusiones, especifique el signo del entero y los tipos de caracteres.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




