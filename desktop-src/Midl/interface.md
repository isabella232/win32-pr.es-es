---
title: interface (atributo)
description: La palabra clave interface especifica el nombre de la interfaz. El nombre de la interfaz debe proporcionarse tanto en el archivo IDL como en el ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- MIDL del atributo de interfaz
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159522"
---
# <a name="interface-attribute"></a>interface (atributo)

La **palabra clave** interface especifica el nombre de la interfaz. El nombre de la interfaz debe proporcionarse tanto en el archivo IDL como en el ACF.

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

*interface-attribute-list* 
</dt> <dd>

Especifica los atributos que se aplican a la interfaz en su conjunto. Los atributos de interfaz válidos para un archivo IDL incluyen el punto de conexión , el objeto local , el objeto , el puntero **\[** [](endpoint.md) **\]** **\[** [](local.md) **\]** **\[** [](object.md) **\]** **\[** [**\_ predeterminado**](pointer-default.md) **\]** , **\[** [**uuid**](uuid.md) **\]** y la **\[** [**versión**](version.md) **\]** . Los atributos de interfaz válidos para un ACF incluyen **\[** [**codificar**](encode.md) **\]** , **\[** [**descodificar**](decode.md), **\]** **\[** [**\_**](auto-handle.md) **\]** **\[** [**\_**](implicit-handle.md) **\]** **\[** [](code.md) **\]** **\[** [](nocode.md) **\]** controlar automáticamente o identificador implícito y código o codificar .

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz. El nombre de la interfaz debe ser un nombre único y debe comenzar con un carácter alfabético o de subrayado.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de la que esta interfaz derivada hereda funciones miembro, códigos de estado y atributos de interfaz. La interfaz derivada no hereda definiciones de tipo. Para ello, use la palabra [**clave import**](import.md) para importar el archivo IDL de la interfaz base.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los nombres de interfaz en el archivo IDL y ACF deben ser los mismos, excepto cuando se usa el modificador del compilador MIDL [**/acf**](-acf.md).

El nombre de la interfaz forma la primera parte del nombre de las estructuras de datos de identificador de interfaz que son parámetros de las funciones en tiempo de ejecución de RPC. Para obtener más información, vea [**RPC \_ IF \_ HANDLE**](/windows/desktop/Rpc/rpc-if-handle).

Si el encabezado de interfaz incluye el atributo de objeto para indicar una interfaz COM, también debe incluir el atributo uuid y debe especificar la interfaz COM base de la que **\[** [](object.md) **\]** **\[** [](uuid.md) **\]** se deriva. Para obtener más información sobre las interfaces COM, vea **\[** [**el objeto**](object.md) **\]** .

También puede usar la palabra clave **interface con** la palabra [**clave typedef**](typedef.md) para definir un tipo de datos de interfaz.

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

[**endpoint**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**valor \_ predeterminado del puntero**](pointer-default.md)
</dt> <dt>

[**RPC \_ IF \_ HANDLE**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 