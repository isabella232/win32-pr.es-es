---
title: switch_type (atributo)
description: El atributo \ switch \_ type\ identifica el tipo de la variable utilizada como discriminador de unión. El tipo de modificador puede ser un tipo entero, de carácter, booleano o de enumeración.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type atributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159366"
---
# <a name="switch_type-attribute"></a>atributo \_ switch type

El **\[ atributo switch \_ type \]** identifica el tipo de la variable utilizada como discriminador de unión. El tipo de modificador puede ser un tipo entero, de carácter, booleano o de enumeración.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*switch-type-specifier* 
</dt> <dd>

Especifica un tipo [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)o [**enum,**](enum.md) o un identificador de este tipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Mientras que **\[ el atributo switch \_ \] type** identifica el tipo de variable, el atributo switch is especifica el nombre del parámetro que es **\[** [**\_**](switch-is.md) el **\]** discriminador de unión. El **\[ atributo switch \_ type \]** se aplica a parámetros o miembros de estructuras o uniones.

La unión y su discriminador deben especificarse en el mismo nivel lógico. Cuando la unión es un parámetro, el discriminador de unión debe ser otro parámetro. Cuando la unión es un campo de una estructura, el discriminador debe ser otro campo de la estructura en el mismo nivel que el campo de unión.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[Uniones no superadas](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ es**](switch-is.md)
</dt> <dt>

[**union**](union.md)
</dt> </dl>

 

 




