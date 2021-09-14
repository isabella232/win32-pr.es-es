---
title: atributo char
description: La palabra clave char especifica un elemento de datos de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- atributo char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159653"
---
# <a name="char-attribute"></a>atributo char

La **palabra clave char** especifica un elemento de datos de 8 bits.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra **clave char** identifica un elemento de datos que tiene 8 bits. Para el compilador MIDL, un **carácter** no tiene signo de forma predeterminada y es sinónimo de [**unsigned**](unsigned.md) **char**.

En esta versión de RPC de Microsoft, las tablas de traducción de caracteres que se convierten entre ASCII y EBCDIC están integradas en las bibliotecas en tiempo de ejecución y el usuario no puede cambiar.

El **tipo char** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El **tipo char** puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador function-return-type y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

Los compiladores de IDL de DCE no aceptan la palabra clave [**signed aplicada**](signed.md) a los **tipos char.** Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/osf del**](-osf.md) compilador de MIDL.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Byte**](byte.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




