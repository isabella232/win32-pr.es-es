---
title: descodificar atributo
description: El atributo \ decode \ ACF especifica que un procedimiento o un tipo necesita compatibilidad de deserialización.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- descodificar el atributo MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358897"
---
# <a name="decode-attribute"></a>descodificar atributo

El atributo **\[ Decode \]** ACF especifica que un procedimiento o un tipo necesita compatibilidad de deserialización.

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en conjunto.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*definición de interfaz* 
</dt> <dd>

Especifica las instrucciones IDL que forman la definición de la interfaz.

</dd> <dt>

*OP-Attribute-List* 
</dt> <dd>

Especifica otros atributos operativos que se aplican al procedimiento como **\[** [**encode**](encode.md) **\]** .

</dd> <dt>

*proc: nombre* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica otros atributos, como **\[** [**encode**](encode.md) **\]** y **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*nombre de tipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Decode \]** hace que el compilador MIDL genere código que una aplicación puede utilizar para recuperar datos serializados de un búfer. El **\[** atributo [**encode**](encode.md) **\]** proporciona compatibilidad de serialización y genera el código para serializar los datos en un búfer.

Use los **\[** atributos [**encode**](encode.md) **\]** y **\[ Decode \]** en un ACF para generar código de serialización para los procedimientos o tipos definidos en el archivo IDL de una interfaz. Cuando se usa como atributo de interfaz, **\[ descodificar \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL. Cuando se usa como atributo de tipo, **\[ descodificar \]** solo se aplica al tipo especificado. Cuando se usa como atributo operativo, **\[ descodificar \]** solo se aplica a ese procedimiento.

Para obtener más información sobre el uso de esta compatibilidad de serialización, vea [servicios de serialización](/windows/desktop/Rpc/serialization-services) y **\[** [**codificación**](encode.md) **\]** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**codificar**](encode.md)
</dt> </dl>

 

 