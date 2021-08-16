---
title: atributo de descodificación
description: El atributo \ decode\ ACF especifica que un procedimiento o un tipo necesita compatibilidad con la deserialización.
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
ms.openlocfilehash: 30c70c821906bcfa4dedb8dbe87aab882866a4f21b7d561b16d3613f9041e0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384737"
---
# <a name="decode-attribute"></a>atributo de descodificación

El **\[ atributo \]** ACF de descodificación especifica que un procedimiento o un tipo necesitan compatibilidad con la deserialización.

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

*interface-attribute-list* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en su conjunto.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instrucciones IDL que forman la definición de la interfaz .

</dd> <dt>

*op-attribute-list* 
</dt> <dd>

Especifica otros atributos operativos que se aplican al procedimiento, como **\[** [**codificar**](encode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica otros atributos, como **\[** [**codificar y**](encode.md) **\]** **\[** [**asignar**](allocate.md) **\]** .

</dd> <dt>

*type-name* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo \] de descodificación** hace que el compilador MIDL genere código que una aplicación puede usar para recuperar datos serializados de un búfer. El **\[** [**atributo de codificación**](encode.md) **\]** proporciona compatibilidad con la serialización, generando el código para serializar los datos en un búfer.

Use los **\[** [**atributos de**](encode.md) **\]** **\[ \]** codificación y descodificación de un ACF para generar código de serialización para procedimientos o tipos definidos en el archivo IDL de una interfaz. Cuando se usa como atributo de interfaz, **\[ la descodificación \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL. Cuando se usa como atributo de tipo, **\[ la descodificación \]** solo se aplica al tipo especificado. Cuando se usa como atributo operativo, **\[ la descodificación \]** solo se aplica a ese procedimiento.

Para obtener más información sobre el uso de esta compatibilidad con la serialización, vea [Servicios de serialización](/windows/desktop/Rpc/serialization-services) y **\[** [**codificación de**](encode.md) **\]** .

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> </dl>

 

 