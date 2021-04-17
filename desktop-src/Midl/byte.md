---
title: byte (atributo)
description: La palabra clave byte especifica un elemento de datos de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- atributo de byte MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651339"
---
# <a name="byte-attribute"></a>byte (atributo)

La palabra clave **byte** especifica un elemento de datos de 8 bits.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un elemento de datos de **bytes** no se somete a ninguna conversión de transmisión en la red como un tipo [**Char**](char-idl.md) .

El tipo de **byte** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El tipo **byte** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

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

[**typedef**](typedef.md)
</dt> </dl>

 

 




