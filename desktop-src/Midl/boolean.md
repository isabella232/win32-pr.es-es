---
title: atributo booleano
description: La palabra clave booleana indica que la expresión o expresión constante asociada al identificador solo toma los valores TRUE y FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- atributo booleano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159670"
---
# <a name="boolean-attribute"></a>atributo booleano

La palabra **clave booleana** indica que la expresión o expresión constante asociada al identificador toma solo los **valores TRUE** y **FALSE.**

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **tipo booleano** es uno de los tipos base del lenguaje IDL. El **tipo booleano** puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador function-return-type y como especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

> [!Note]  
> El **tipo** base booleano no es compatible con el [**atributo oleautomation.**](oleautomation.md) Use VARIANT \_ BOOL en las interfaces compatibles con Automation.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




