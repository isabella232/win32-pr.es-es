---
title: atributo local
description: El atributo \ local\ especifica al compilador MIDL que una interfaz o función no es remota.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- MIDL del atributo local
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159508"
---
# <a name="local-attribute"></a>atributo local

El **\[ atributo local \]** especifica al compilador MIDL que una interfaz o función no es remota.

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

*interface-attribute-list* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en su conjunto. El punto de **\[** [**conexión de**](endpoint.md) **\]** **\[** [](version.md) **\]** atributos, la versión y el **\[** [**valor predeterminado \_ del**](pointer-default.md) **\]** puntero son opcionales. Al compilar con el modificador [**/app \_ config,**](-app-config.md) también puede haber un identificador **\[** [**\_ implícito**](implicit-handle.md) o un identificador **\]** **\[** [**\_**](auto-handle.md) **\]** automático. Separe varios atributos con comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre por el que los componentes de software pueden delinear la interfaz.

</dd> <dt>

*string-uuid* 
</dt> <dd>

Especifica una cadena UUID generada por la utilidad Uuidgen. Si no usa el modificador del compilador MIDL [**/osf**](-osf.md), puede incluir la cadena UUID entre comillas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada; el atributo de puntero **\[** [](callback.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto . Separe varios atributos con comas.

</dd> <dt>

*function-declarator* 
</dt> <dd>

Especifica el especificador de tipo, el nombre de función y la lista de parámetros de la función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo local \]** se puede aplicar a funciones individuales o a la interfaz en su conjunto.

Cuando se usa en el encabezado de interfaz, el atributo **\[ local \]** permite usar el compilador MIDL como generador de encabezados. El compilador no genera código auxiliar para ninguna función y no garantiza que se pueda transmitir el encabezado.

Para una interfaz RPC, el **\[ atributo local \]** no se puede usar al mismo tiempo que el atributo **\[** [**uuid.**](uuid.md) **\]** Uuid **\[ o \]** **\[ local \]** deben estar presentes en el encabezado de interfaz y el que elija debe producirse exactamente una vez.

Para una interfaz COM (identificada por el atributo de interfaz de objeto), la lista de atributos de interfaz puede incluir el atributo **\[** [](object.md) **\]** **\[ local \]** aunque el **\[** [**atributo uuid**](uuid.md) **\]** esté presente.

Cuando se usa en una función individual, el atributo **\[ local \]** designa un procedimiento local para el que no se genera ningún código auxiliar. El **\[ uso de local \]** como atributo de función es una extensión de Microsoft para DCE IDL. Por lo tanto, este atributo no está disponible cuando se compila mediante el modificador MIDL [**/osf.**](-osf.md)

Tenga en cuenta que una interfaz sin atributos se puede importar en un archivo IDL base. Sin embargo, la interfaz solo debe contener tipos de datos sin procedimientos. Si incluso hay un procedimiento contenido en la interfaz, se debe especificar un atributo uuid o local.

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

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**valor \_ predeterminado del puntero**](pointer-default.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 




