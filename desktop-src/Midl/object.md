---
title: object (atributo)
description: El atributo \ object\ interface identifica una interfaz COM.
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
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383513"
---
# <a name="object-attribute"></a>object (atributo)

El **\[ atributo de \]** interfaz de objeto identifica una interfaz COM. (Una lista de atributos de interfaz que no incluye el atributo **\[ de \]** objeto indica una interfaz RPC de DCE).

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

*string-uuid* 
</dt> <dd>

Cadena UUID generada por la utilidad Uuidgen. Puede incluir la cadena UUID entre comillas.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la interfaz en su conjunto.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Interfaz COM de la que deriva esta interfaz. La interfaz base debe ser [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)u otra interfaz COM que derive, directa o indirectamente, de **IUnknown** **o IDispatch.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una lista de atributos de interfaz para una interfaz COM debe incluir **\[** [**el atributo uuid,**](uuid.md) **\]** pero no puede incluir el atributo **\[** [**de**](version.md) **\]** versión.

De forma predeterminada, la compilación de una interfaz COM con el compilador MIDL genera los archivos necesarios para compilar un archivo DLL de proxy. Este archivo DLL contiene el código para admitir el uso de la interfaz COM personalizada tanto por las aplicaciones cliente como por los servidores de objetos. Sin embargo, si la lista de atributos de interfaz para una interfaz COM especifica el atributo local, el compilador MIDL genera solo el archivo de encabezado **\[** [](local.md) **\]** de interfaz.

El compilador MIDL genera automáticamente un tipo de datos de interfaz para una interfaz COM. Como alternativa, puede usar [**typedef**](typedef.md) con la palabra clave [**interface**](interface.md) para definir explícitamente un tipo de datos de interfaz. A continuación, la especificación de interfaz puede usar el tipo de datos de interfaz en parámetros de función y valores devueltos, miembros [**struct**](struct.md) [**y union,**](union.md) y otras declaraciones de tipo. En el ejemplo siguiente se muestra el uso de un tipo de datos [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) generado automáticamente:

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

En una interfaz COM, se supone que todas las funciones miembro de interfaz son funciones virtuales. Una función virtual tiene un puntero **this implícito** como primer parámetro. La tabla de funciones virtuales contiene una entrada para cada función miembro de interfaz.

Las funciones miembro de la interfaz de objeto no **\[** [**local**](local.md) **\]** deben tener un valor devuelto de HRESULT o SCODE. (Tenga en cuenta que las versiones anteriores de MIDL permitían que las funciones miembro devolvieron [**void**](void.md). Sin embargo, a partir de midl versión 3.0, devolver **void** genera un error del compilador). Tener un valor devuelto de HRESULT o SCODE significa que si se genera una excepción durante una llamada remota, los servidores proxy generados detectan la excepción y devuelven el código de excepción en el valor devuelto. Si la aplicación puede permitirse omitir los errores que se producen durante una llamada a procedimiento remoto, puede especificar HRESULT como tipo de valor devuelto sin comprobar el valor devuelto después de la llamada.

Si va a volver a compilar una aplicación antigua, el cambio de los tipos de valor devuelto puede presentar problemas de compatibilidad con versiones anteriores cuando el servidor envía el resultado recién introducido al cliente. Como alternativa a cambiar el tipo de valor devuelto, puede etiquetar la función que devuelve [**void**](void.md) con la llamada como atributo, lo que la convierte en una **\[** [**\_**](call-as.md) **\]** función local. A continuación, defina una función remota relacionada con los mismos parámetros, pero con el tipo de valor devuelto HRESULT. La función local puede generar una excepción basada en ese valor HRESULT, si es necesario.

El **\[ atributo \]** de objeto no está disponible cuando se compila mediante el modificador [**/osf del**](-osf.md) compilador de MIDL.

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

[**llamar \_ a como**](call-as.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**iid \_ es**](iid-is.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 