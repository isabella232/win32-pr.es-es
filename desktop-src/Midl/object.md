---
title: object (atributo)
description: El atributo \ Object \ interface identifica una interfaz COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- atributo de objeto MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb2c21246282646dcf6ae488411316e07ab62b2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790900"
---
# <a name="object-attribute"></a>object (atributo)

El atributo de interfaz de **\[ objeto \]** identifica una interfaz com. (Una lista de atributos de interfaz que no incluye el atributo de **\[ objeto \]** indica una interfaz RPC de DCE).

``` syntax
[ 
    object, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
...    
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*cadena: UUID* 
</dt> <dd>

Cadena UUID generada por la utilidad Uuidgen. Puede incluir la cadena UUID entre comillas.

</dd> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Otros atributos que se aplican a la interfaz en conjunto.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

La interfaz COM de la que se deriva esta interfaz. La interfaz base debe ser [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)u otra interfaz com que deriva, ya sea directa o indirectamente, de **IUnknown** o **IDispatch**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una lista de atributos de interfaz para una interfaz COM debe incluir el **\[** atributo [**UUID**](uuid.md) **\]** , pero no puede incluir el **\[** [](version.md) **\]** atributo version.

De forma predeterminada, al compilar una interfaz COM con el compilador MIDL se generan los archivos necesarios para compilar un archivo DLL de proxy. Este archivo DLL contiene el código para admitir el uso de la interfaz COM personalizada por parte de las aplicaciones cliente y los servidores de objetos. Sin embargo, si la lista de atributos de interfaz para una interfaz COM especifica el **\[** [](local.md) **\]** atributo local, el compilador MIDL solo genera el archivo de encabezado de interfaz.

El compilador MIDL genera automáticamente un tipo de datos de interfaz para una interfaz COM. Como alternativa, puede usar [**typedef**](typedef.md) con la palabra clave [**interface**](interface.md) para definir explícitamente un tipo de datos de interfaz. La especificación de la interfaz puede usar el tipo de datos de la interfaz en los parámetros de función y los valores devueltos, los miembros de [**estructura**](struct.md) y [**Unión**](union.md) y otras declaraciones de tipos. En el ejemplo siguiente se muestra el uso de un tipo de datos [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) generado automáticamente:

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

En una interfaz COM, se supone que todas las funciones miembro de interfaz son funciones virtuales. Una función virtual tiene un puntero **this** implícito como primer parámetro. La tabla de función Virtual contiene una entrada para cada función miembro de interfaz.

**\[**[](local.md) **\]** Las funciones miembro de la interfaz de objeto no local deben tener un valor devuelto de HRESULT o SCODE. (Tenga en cuenta que las versiones anteriores de MIDL permitían que las funciones miembro devuelvan [**void**](void.md). Sin embargo, a partir de la versión 3,0 de MIDL, si se devuelve **void** , se genera un error del compilador. Tener un valor devuelto de HRESULT o SCODE significa que si se genera una excepción durante una llamada remota, los proxies generados detectan la excepción y devuelven el código de excepción en el valor devuelto. Si la aplicación puede permitirse omitir los errores que se producen durante una llamada a procedimiento remoto, puede especificar HRESULT como el tipo de valor devuelto sin comprobar el valor devuelto después de la llamada.

Si va a volver a compilar una aplicación antigua, el cambio de los tipos de valor devueltos puede presentar problemas de compatibilidad con versiones anteriores cuando el servidor envía el resultado recién introducido al cliente. Como alternativa al cambio del tipo de valor devuelto, puede etiquetar la función que devuelve [**void**](void.md) con el **\[** atributo [**Call \_ as**](call-as.md) , lo que lo **\]** convierte en una función local. A continuación, defina una función remota relacionada con los mismos parámetros pero con el tipo de valor devuelto HRESULT. La función local puede producir una excepción basada en ese valor HRESULT, si es necesario.

El atributo de **\[ \] objeto** no está disponible al compilar mediante el modificador [**/OSF**](-osf.md) del compilador MIDL.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**llamar a \_ como**](call-as.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**IID \_ es**](iid-is.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 