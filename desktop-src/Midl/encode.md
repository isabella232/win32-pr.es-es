---
title: atributo de codificación
description: El atributo \ encode\ ACF especifica que un procedimiento o un tipo de datos necesita compatibilidad con la serialización.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- codificar el atributo MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159603"
---
# <a name="encode-attribute"></a>atributo de codificación

El **\[ atributo \]** ACF de codificación especifica que un procedimiento o un tipo de datos necesita compatibilidad con la serialización.

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
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

Especifica otros atributos operativos que se aplican al procedimiento, como **\[** [**descodificar**](decode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica otros atributos que se aplican al tipo, como **\[** [**descodificar y**](decode.md) **\]** **\[** [**asignar**](allocate.md) **\]** .

</dd> <dt>

*type-name* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \] de codificación** hace que el compilador MIDL genere código que una aplicación puede usar para serializar los datos en un búfer. El **\[** [**atributo de descodificación**](decode.md) **\]** genera el código para desmarque los datos de un búfer.

Use los **\[ atributos de codificación \]** y descodificación en un ACF para generar código de serialización para procedimientos o tipos definidos en el archivo **\[** [](decode.md) **\]** IDL de una interfaz. Cuando se usa como atributo de interfaz, **\[ la codificación \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL. Cuando se usa como atributo operativo, **\[ la codificación \]** solo se aplica al procedimiento especificado. Cuando se usa como atributo de tipo, **\[ la codificación \]** solo se aplica al tipo especificado.

Cuando el atributo **\[ de \]** codificación o descodificación se aplica a un procedimiento, el compilador MIDL genera un código auxiliar de serialización de forma similar a como se generan códigos auxiliares remotos para **\[** [](decode.md) **\]** rutinas remotas. Un procedimiento puede ser remoto o serializador, pero no puede ser ambos. El prototipo de la rutina generada se envía al CÓDIGO AUXILIAR. Archivo H mientras el propio código auxiliar entra en el \_ archivo STUB C.C.

El compilador MIDL **\[ \]** genera dos funciones para cada tipo al que se aplica el atributo de codificación y una función adicional para cada tipo al que se **\[** [](decode.md) **\]** aplica el atributo de descodificación. Por ejemplo, para un tipo definido por el usuario denominado MyType, el compilador genera código para las funciones MyType \_ Encode, MyType Decode y \_ MyType \_ AlignSize. Para estas funciones, el compilador escribe prototipos en STUB. H y código fuente a STUB \_ C.C.

Para obtener información adicional sobre los identificadores de serialización y la codificación o la codificación de datos, vea [Servicios de serialización](/windows/desktop/Rpc/serialization-services).

## <a name="examples"></a>Ejemplos

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Decodificar**](decode.md)
</dt> </dl>

 

 