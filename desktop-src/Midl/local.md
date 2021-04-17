---
title: atributo local
description: El atributo \ local \ especifica al compilador de MIDL que una interfaz o una función no es remota.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- atributo local MIDL
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665755"
---
# <a name="local-attribute"></a>atributo local

El atributo **\[ local \]** especifica al compilador de MIDL que una interfaz o función no es remota.

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en conjunto. Los atributos **\[** [**Endpoint**](endpoint.md) **\]** , **\[** [**version**](version.md) **\]** y **\[** [**Pointer \_ default**](pointer-default.md) **\]** son opcionales. Al compilar con el modificador de [**\_ configuración/App**](-app-config.md) , **\[** también puede haber un [**\_ identificador implícito**](implicit-handle.md) **\]** o un **\[** [**\_ identificador automático**](auto-handle.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre por el que los componentes de software pueden delimitar la interfaz.

</dd> <dt>

*cadena: UUID* 
</dt> <dd>

Especifica una cadena de UUID generada por la utilidad Uuidgen. Si no usa el modificador de compilador de MIDL [**/OSF**](-osf.md), puede escribir la cadena de UUID entre comillas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*function-declarator* 
</dt> <dd>

Especifica el especificador de tipo, el nombre de función y la lista de parámetros para la función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ local \]** se puede aplicar a funciones individuales o a la interfaz en conjunto.

Cuando se usa en el encabezado de la interfaz, el atributo **\[ local \]** permite usar el compilador MIDL como generador de encabezados. El compilador no genera código auxiliar para ninguna función y no garantiza que se pueda transmitir el encabezado.

En el caso de una interfaz RPC, el atributo **\[ local \]** no se puede usar al mismo tiempo que el **\[** atributo [**UUID**](uuid.md) **\]** . **\[ UUID \]** o **\[ local \]** deben estar presentes en el encabezado de la interfaz y el que elija debe aparecer exactamente una vez.

En el caso de una interfaz COM (identificada por el atributo de la interfaz de **\[** [**objeto**](object.md) **\]** ), la lista de atributos de interfaz puede incluir el atributo **\[ local \]** aunque el **\[** atributo [**UUID**](uuid.md) **\]** esté presente.

Cuando se usa en una función individual, el atributo **\[ local \]** designa un procedimiento local para el que no se genera ningún código auxiliar. Usar **\[ local \]** como atributo de función es una extensión de Microsoft para DCE IDL. Por lo tanto, este atributo no está disponible al compilar mediante el modificador [**/OSF**](-osf.md) de MIDL.

Tenga en cuenta que una interfaz sin atributos se puede importar en un archivo IDL base. Sin embargo, la interfaz debe contener solo tipos de contenido sin procedimientos. Si hay un procedimiento incluido en la interfaz, se debe especificar un atributo local o UUID.

## <a name="examples"></a>Ejemplos

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**puntero \_ predeterminado**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 




