---
title: Atributo booleano
description: La palabra clave Boolean indica que la expresión o expresión constante asociada con el identificador solo toma los valores TRUE y FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- Atributo booleano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419617"
---
# <a name="boolean-attribute"></a>Atributo booleano

La palabra clave **Boolean** indica que la expresión o expresión constante asociada con el identificador solo toma los valores **true** y **false**.

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El tipo **booleano** es uno de los tipos base del lenguaje IDL. El tipo **Boolean** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

> [!Note]  
> El tipo base **booleano** no es compatible con el atributo [**oleautomation**](oleautomation.md) . Use VARIANT \_ bool en las interfaces compatibles con Automation.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




