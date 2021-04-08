---
title: atributo switch
description: La palabra clave switch selecciona el discriminante de una Unión encapsulada \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- atributo de modificador MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994733"
---
# <a name="switch-attribute"></a>atributo switch

La palabra clave **Switch** selecciona el discriminante de una [**\_ Unión encapsulada**](encapsulated-unions.md).

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de conmutador* 
</dt> <dd>

Especifica un tipo [**int**](int.md), [**Char**](-char.md), [**enum**](enum.md) o un identificador que se resuelve en uno de estos tipos.

</dd> <dt>

*cambiar nombre* 
</dt> <dd>

Especifica el nombre de la variable de tipo *Switch-Type* que actúa como discriminante de Unión.

</dd> </dl>

## <a name="examples"></a>Ejemplos

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Uniones no encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**el modificador \_ es**](switch-is.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> <dt>

[**Unión**](union.md)
</dt> </dl>

 

 




