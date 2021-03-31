---
title: wchar_t atributo)
description: La \_ palabra clave WCHAR t designa un tipo de caracteres anchos.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t el atributo MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2020
ms.locfileid: "104077408"
---
# <a name="wchar_t-attribute"></a>WCHAR \_ t (atributo)

La palabra clave **WCHAR \_ t** designa un tipo de caracteres anchos.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El tipo **WCHAR \_ t** lo define MIDL como un objeto de datos [**Short**](short.md) (de 16 bits) [**sin signo**](unsigned.md) .

El compilador MIDL permite la redefinición de **WCHAR \_ t**, pero solo si es coherente con la definición anterior.

El tipo de carácter ancho es uno de los tipos predefinidos de MIDL. El tipo de caracteres anchos puede aparecer como un especificador de tipo en las declaraciones [**const**](const.md) , en las declaraciones [**typedef**](typedef.md) , en las declaraciones generales y en los declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

El atributo de **\[ cadena \]** se puede aplicar a un puntero o una matriz de tipo **WCHAR \_ t**.

Use el carácter **L** delante de un carácter o una constante de cadena para designar la constante de tipo de carácter ancho.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> </dl>

 

 




