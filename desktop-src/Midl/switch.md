---
title: atributo switch
description: La palabra clave switch selecciona el discriminador para una unión \_ encapsulada.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- atributo switch MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159365"
---
# <a name="switch-attribute"></a>atributo switch

La palabra clave **switch** selecciona el discriminador para una [**unión \_ encapsulada.**](encapsulated-unions.md)

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*switch-type* 
</dt> <dd>

Especifica un [**tipo int,**](int.md) [**char,**](-char.md) [**enum**](enum.md) o un identificador que se resuelve en uno de estos tipos.

</dd> <dt>

*switch-name* 
</dt> <dd>

Especifica el nombre de la variable de tipo *switch-type* que actúa como discriminador de unión.

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

[Uniones no superadas](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ es**](switch-is.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> <dt>

[**union**](union.md)
</dt> </dl>

 

 




