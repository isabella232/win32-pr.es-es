---
title: interface (atributo)
description: La palabra clave interface especifica el nombre de la interfaz. El nombre de la interfaz debe proporcionarse en el archivo IDL y en el ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- atributo de interfaz MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904536"
---
# <a name="interface-attribute"></a>interface (atributo)

La palabra clave **interface** especifica el nombre de la interfaz. El nombre de la interfaz debe proporcionarse en el archivo IDL y en el ACF.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica los atributos que se aplican a la interfaz en conjunto. Los atributos de interfaz válidos para un archivo IDL incluyen el **\[** [**punto de conexión**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**objeto**](object.md) **\]** , **\[** [**\_ valor predeterminado del puntero**](pointer-default.md), **\]** **\[** [**UUID**](uuid.md) **\]** y **\[** [**versión**](version.md) **\]** . Los atributos de interfaz válidos para un ACF incluyen **\[** [**codificación**](encode.md) **\]** , **\[** [**descodificación**](decode.md) **\]** , **\[** [**\_ identificador automático**](auto-handle.md) **\]** o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** , y **\[** [**código**](code.md) **\]** o **\[** [**nocode**](nocode.md) **\]** .

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz. El nombre de la interfaz debe ser un nombre único y debe comenzar por un carácter alfabético o de subrayado.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de la que esta interfaz derivada hereda las funciones miembro, los códigos de estado y los atributos de interfaz. La interfaz derivada no hereda las definiciones de tipo. Para ello, use la palabra clave [**Import**](import.md) para importar el archivo IDL de la interfaz base.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los nombres de interfaz en el archivo IDL y ACF deben ser los mismos, excepto cuando se usa el modificador de compilador MIDL [**/ACF**](-acf.md).

El nombre de la interfaz forma la primera parte del nombre de las estructuras de datos de identificador de interfaz que son parámetros de las funciones en tiempo de ejecución de RPC. Para obtener más información, vea [**RPC \_ If \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).

Si el encabezado de la interfaz incluye el **\[** [](object.md) **\]** atributo de objeto para indicar una interfaz com, también debe incluir el **\[** atributo [**UUID**](uuid.md) **\]** y debe especificar la interfaz com base de la que se deriva. Para obtener más información sobre las interfaces COM, vea **\[** [**Object**](object.md) **\]** .

También puede utilizar la palabra clave **interface** con la palabra clave [**typedef**](typedef.md) para definir un tipo de datos de interfaz.

## <a name="examples"></a>Ejemplos

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**puntero \_ predeterminado**](pointer-default.md)
</dt> <dt>

[**identificador de RPC \_ If \_**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 