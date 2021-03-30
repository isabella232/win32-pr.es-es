---
title: Char (atributo)
description: La palabra clave char especifica un elemento de datos de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- Char (atributo) MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904198"
---
# <a name="char-attribute"></a>Char (atributo)

La palabra clave **Char** especifica un elemento de datos de 8 bits.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra clave **Char** identifica un elemento de datos que tiene 8 bits. En el compilador de MIDL, un **carácter** no tiene signo de forma predeterminada y es sinónimo de **carácter** [**sin signo**](unsigned.md) .

En esta versión de Microsoft RPC, las tablas de traducción de caracteres que se convierten entre ASCII y EBCDIC están integradas en las bibliotecas en tiempo de ejecución y el usuario no puede cambiarlas.

El tipo **Char** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El tipo **Char** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

Los compiladores de DCE IDL no aceptan la palabra clave [**signed**](signed.md) aplicada a tipos **Char** . Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**bytes**](byte.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




