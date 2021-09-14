---
title: atributo decode
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
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159632"
---
# <a name="decode-attribute"></a>atributo decode

El **\[ atributo \] ACF** de descodificación especifica que un procedimiento o un tipo necesita compatibilidad con la deserialización.

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

## <a name="remarks"></a>Observaciones

El **\[ atributo \] de descodificación** hace que el compilador MIDL genere código que una aplicación puede usar para recuperar datos serializados de un búfer. El **\[** [**atributo de codificación**](encode.md) **\]** proporciona compatibilidad con la serialización, generando el código para serializar los datos en un búfer.

Use los **\[** [**atributos de**](encode.md) **\]** **\[ \]** codificación y descodificación en un ACF para generar código de serialización para procedimientos o tipos definidos en el archivo IDL de una interfaz. Cuando se usa como atributo de interfaz, **\[ la descodificación \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL. Cuando se usa como atributo de tipo, **\[ la descodificación \]** solo se aplica al tipo especificado. Cuando se usa como atributo operativo, **\[ la descodificación \]** solo se aplica a ese procedimiento.

Para obtener más información sobre el uso de esta compatibilidad con la serialización, vea [Servicios de serialización](/windows/desktop/Rpc/serialization-services) **\[** [**y codificación de**](encode.md) **\]** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> </dl>

 

 