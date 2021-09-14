---
title: atributo byte
description: La palabra clave byte especifica un elemento de datos de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- atributo byte MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159663"
---
# <a name="byte-attribute"></a>atributo byte

La **palabra clave byte** especifica un elemento de datos de 8 bits.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un **elemento de** datos byte no se somete a ninguna conversión para la transmisión en la red como podría ser un tipo [**char.**](char-idl.md)

El **tipo byte** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El **tipo de** byte puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador function-return-type y como especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

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

[**Typedef**](typedef.md)
</dt> </dl>

 

 




