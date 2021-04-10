---
title: atributo encode
description: El atributo \ encode \ ACF especifica que un procedimiento o un tipo de datos necesita compatibilidad de serialización.
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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995135"
---
# <a name="encode-attribute"></a>atributo encode

El atributo **\[ encode \]** ACF especifica que un procedimiento o un tipo de datos necesita compatibilidad de serialización.

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

Especifica otros atributos operativos que se aplican al procedimiento como **\[** [**descodificar**](decode.md) **\]** .

</dd> <dt>

*proc: nombre* 
</dt> <dd>

Especifica el nombre del procedimiento.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica otros atributos que se aplican al tipo, como **\[** [**Decode**](decode.md) **\]** y **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*nombre de tipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ encode \]** hace que el compilador MIDL genere código que una aplicación puede utilizar para serializar los datos en un búfer. El **\[** atributo [**Decode**](decode.md) **\]** genera el código para calcular las referencias de los datos de un búfer.

Use los atributos **\[ encode \]** y **\[** [**Decode**](decode.md) **\]** en un ACF para generar código de serialización para los procedimientos o tipos definidos en el archivo IDL de una interfaz. Cuando se usa como atributo de interfaz, **\[ encode \]** se aplica a todos los tipos y procedimientos definidos en el archivo IDL. Cuando se usa como atributo operativo, **\[ encode \]** solo se aplica al procedimiento especificado. Cuando se usa como atributo de tipo, **\[ encode \]** solo se aplica al tipo especificado.

Cuando se aplica el atributo de **\[ codificación \]** o **\[** [**descodificación**](decode.md) **\]** a un procedimiento, el compilador MIDL genera un código auxiliar de serialización de forma similar a como se generan los códigos auxiliares remotos para las rutinas remotas. Un procedimiento puede ser un procedimiento remoto o de serialización, pero no puede ser ambos. El prototipo de la rutina generada se envía al código auxiliar. H mientras el propio código auxiliar entra en el \_ archivo stub c. c.

El compilador MIDL genera dos funciones para cada tipo al que se aplica el atributo **\[ \] encode** y una función adicional para cada tipo al **\[** que se aplica el atributo [**descode**](decode.md) **\]** . Por ejemplo, para un tipo definido por el usuario denominado mi tipo, el compilador genera código para las \_ funciones de codificación, \_ descodificación y tipo \_ AlignSize. Para estas funciones, el compilador escribe prototipos en STUB. H y código fuente para STUB \_ C.C.

Para obtener más información sobre los identificadores de serialización y la codificación o descodificación de datos, vea [servicios de serialización](/windows/desktop/Rpc/serialization-services).

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

[**descodificar**](decode.md)
</dt> </dl>

 

 