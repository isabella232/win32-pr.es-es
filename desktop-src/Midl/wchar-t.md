---
title: wchar_t atributo
description: La palabra clave wchar \_ t designa un tipo de caracteres anchos.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t atributo MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159317"
---
# <a name="wchar_t-attribute"></a>Atributo wchar \_ t

La **palabra clave wchar \_ t** designa un tipo de caracteres anchos.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

MIDL define el tipo **\_ wchar t** como [**un objeto**](unsigned.md) de datos corto [**sin**](short.md) signo (16 bits).

El compilador MIDL permite la redefinición **de wchar \_ t,** pero solo si es coherente con la definición anterior.

El tipo de carácter ancho es uno de los tipos predefinidos de MIDL. El tipo de caracteres anchos puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

El **\[ atributo \]** de cadena se puede aplicar a un puntero o matriz de tipo **wchar \_ t**.

Use el **carácter L** antes de un carácter o una constante de cadena para designar la constante de tipo de carácter ancho.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




