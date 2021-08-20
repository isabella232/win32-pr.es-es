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
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013553"
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

[**Unión**](union.md)
</dt> </dl>

 

 




