---
title: async_uuid (atributo)
description: El atributo \ Async \_ UUID \ interface indica al compilador de MIDL que defina las versiones sincrónicas y asincrónicas de una interfaz com.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid el atributo MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fd7b4d9d9bf7a595415e55de778a419d91051c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149220"
---
# <a name="async_uuid-attribute"></a>\_atributo de UUID Async

El atributo **\[ Async \_ UUID \]** interface indica al compilador de MIDL que defina las versiones sincrónicas y asincrónicas de una interfaz com.

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

*cadena: uuid1* 
</dt> <dd>

Cadena UUID, generada por la utilidad uuidgen, que identifica la versión sincrónica de la interfaz.

</dd> <dt>

*cadena: uuid2* 
</dt> <dd>

Cadena UUID, generada por la utilidad uuidgen, que identifica la versión asincrónica de la interfaz.

</dd> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Otros atributos que se aplican a la interfaz en conjunto. No se puede usar el atributo [**\[ version \]**](version.md) en una interfaz com.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

La interfaz de la que se deriva esta interfaz. La interfaz base debe ser **IUnknown** o una interfaz asincrónica que deriva, ya sea directa o indirectamente, de **IUnknown**.

</dd> <dt>

*definición de interfaz* 
</dt> <dd>

Especifica las instrucciones IDL que forman la definición de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de este atributo requiere Windows 2000 o versiones posteriores de Windows.

Al aplicar el atributo de **\[ \_ UUID \] asincrónico** a una interfaz com (es decir, una interfaz que tiene el atributo de [**\[ objeto \]**](object.md) ), el compilador MIDL genera una definición asincrónica de la interfaz, además de la versión sincrónica tradicional. La interfaz asincrónica tendrá los mismos nombres que la interfaz sincrónica, pero con un prefijo "Async". El identificador de interfaz (IID) será el UUID especificado como un parámetro para el atributo **\[ Async \_ UUID \]** .

En el caso de la interfaz asincrónica, MIDL divide cada método en métodos independientes de *Inicio* y *finalización* . El método *Begin* tiene el nombre de método sincrónico con un \_ prefijo "begin" e incluye todos los parámetros [**\[ in \]**](in.md) del método sincrónico. El método *Finish* tiene el nombre del método sincrónico con un \_ prefijo "Finish" e incluye todos los parámetros [**\[ out \]**](out-idl.md) del método sincrónico. Si el método sincrónico tiene un parámetro **\[ in, out \] ,** se incluirán en los métodos asincrónicos de *Inicio* y *finalización* .

Si un método de interfaz asincrónica tiene la [**\[ llamada \_ como \]**](call-as.md) atributo, MIDL generará declaraciones para los métodos *Begin* y *Finish* . Debe implementar ambos métodos.

Cada interfaz asincrónica es un modificador en una interfaz sincrónica y, como tal, no tiene un gráfico de herencia independiente. Esto significa que no se puede definir una interfaz sincrónica a partir de una interfaz asincrónica (distinta de **IUnknown**). Ni las interfaces sincrónicas se pueden heredar de interfaces asincrónicas. El compilador MIDL emitirá un mensaje de error si se intenta cualquiera de ellos.

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

[**llamar a \_ como**](call-as.md)
</dt> <dt>

[**IID \_ es**](iid-is.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 