---
title: switch_type (atributo)
description: El atributo \ switch \_ Type \ identifica el tipo de la variable que se usa como discriminante de Unión. El tipo de modificador puede ser un entero, un carácter, un valor booleano o un tipo de enumeración.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type el atributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904129"
---
# <a name="switch_type-attribute"></a>atributo de tipo de conmutador \_

El atributo de **\[ \_ tipo \] de conmutador** identifica el tipo de la variable que se usa como discriminante de Unión. El tipo de modificador puede ser un entero, un carácter, un valor booleano o un tipo de enumeración.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Switch-Type-Specifier* 
</dt> <dd>

Especifica un tipo [**int**](int.md), [**Char**](char-idl.md), [**Boolean**](boolean.md)o [**enum**](enum.md) , o un identificador de este tipo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Mientras que el atributo de **\[ \_ tipo \] de conmutador** identifica el tipo de variable, el **\[** atributo [**Switch \_ es**](switch-is.md) **\]** especifica el nombre del parámetro que es la Unión discriminante. El atributo de **\[ \_ tipo \] de conmutador** se aplica a los parámetros o miembros de estructuras o uniones.

La Unión y su discriminante deben especificarse en el mismo nivel lógico. Cuando la Unión es un parámetro, el discriminante de Unión debe ser otro parámetro. Cuando la Unión es un campo de una estructura, el discriminante debe ser otro campo de la estructura en el mismo nivel que el campo de Unión.

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

[**Booleano**](boolean.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[Uniones no encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**el modificador \_ es**](switch-is.md)
</dt> <dt>

[**Unión**](union.md)
</dt> </dl>

 

 




