---
title: async_uuid (atributo)
description: El atributo de interfaz \ async uuid\ dirige al compilador MIDL para definir las versiones sincrónicas y \_ asincrónicas de una interfaz COM.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid atributo MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a784cadf470fa312a82e473f3934dbda1a2b6dce20d2ae34c7074c309398cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808239"
---
# <a name="async_uuid-attribute"></a>Atributo \_ uuid asincrónico

El **\[ atributo de interfaz \_ uuid \]** asincrónica dirige al compilador MIDL para definir las versiones sincrónicas y asincrónicas de una interfaz COM.

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string-uuid1* 
</dt> <dd>

Cadena UUID generada por la utilidad Uuidgen, que identifica la versión sincrónica de la interfaz.

</dd> <dt>

*string-uuid2* 
</dt> <dd>

Cadena UUID generada por la utilidad Uuidgen, que identifica la versión asincrónica de la interfaz.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la interfaz en su conjunto. No se puede usar el [**\[ atributo version \]**](version.md) en una interfaz COM.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Interfaz de la que deriva esta interfaz. La interfaz base debe ser **IUnknown** o una interfaz asincrónica que derive, directa o indirectamente, de **IUnknown**.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instrucciones IDL que forman la definición de la interfaz .

</dd> </dl>

## <a name="remarks"></a>Comentarios

El uso de este atributo requiere Windows 2000 o versiones posteriores de Windows.

Al aplicar el atributo **\[ \_ uuid \]** asincrónico a una interfaz COM (es decir, [**\[ \]**](object.md) una interfaz que tiene el atributo de objeto), el compilador midL genera una definición asincrónica de la interfaz, además de la versión sincrónica tradicional. La interfaz asincrónica tendrá los mismos nombres que la interfaz sincrónica, pero con un prefijo "Async". El identificador de interfaz (IID) será el UUID especificado como parámetro para el atributo **\[ \_ uuid \] asincrónico.**

Para la interfaz asincrónica, MIDL divide cada método en métodos *de inicio* *y fin* independientes. El *método begin* tiene el nombre del método sincrónico con un prefijo "Begin" e incluye todos los parámetros \_ [**\[ in \]**](in.md) del método sincrónico. El *método finish* tiene el nombre del método sincrónico con el prefijo "Finish" e incluye todos los parámetros \_ [**\[ out \]**](out-idl.md) del método sincrónico. Si el método sincrónico tiene alguna **\[ entrada, \] los** parámetros out se incluirán en los métodos asincrónicos *begin* *y finish.*

Si un método de interfaz asincrónica tiene [**\[ la llamada \_ como \]**](call-as.md) atributo, MIDL generará declaraciones para los métodos *begin* y *finish.* Debe implementar ambos métodos.

Cada interfaz asincrónica es un modificador en una interfaz sincrónica y, como tal, no tiene un gráfico de herencia independiente. Esto significa que no se puede definir una interfaz sincrónica desde una interfaz asincrónica (que no **sea IUnknown**). Las interfaces sincrónicas tampoco pueden heredar de interfaces asincrónicas. El compilador MIDL emitirá un mensaje de error si intenta cualquiera de ellos.

## <a name="examples"></a>Ejemplos

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definición de interfaces COM](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**llamar \_ a como**](call-as.md)
</dt> <dt>

[**iid \_ es**](iid-is.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 