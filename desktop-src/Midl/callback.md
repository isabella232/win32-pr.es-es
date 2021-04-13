---
title: atributo callback
description: El atributo \ callback \ declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida. Las funciones de devolución de llamada proporcionan una manera para que el servidor ejecute código en el cliente.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- atributo de devolución de llamada MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420650"
---
# <a name="callback-attribute"></a>atributo callback

El atributo **\[ callback \]** declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida. Las funciones de devolución de llamada proporcionan una manera para que el servidor ejecute código en el cliente.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**locales**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [ \_ tipo base](midl-base-types.md), [**un struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*PTR-declarador* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> <dt>

*clara* 
</dt> <dd>

Especifica un declarador de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). El identificador de nombre de parámetro es opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función de **\[ devolución de llamada \]** es útil cuando el servidor debe obtener información del cliente. Si se admiten aplicaciones de servidor en Windows 3. *x*, el servidor podría hacer una llamada a un procedimiento remoto en Windows 3. *x* servidor para obtener la información necesaria. La función de devolución de llamada logra el mismo propósito y permite que el servidor consulte al cliente información en el contexto de la llamada original.

Las devoluciones de llamada son casos especiales de llamadas remotas que se ejecutan como parte de un único subproceso. Se emite una devolución de llamada en el contexto de una llamada remota. Cualquier procedimiento remoto definido como parte de la misma interfaz que la función de devolución de llamada estática puede llamar a la función de devolución de llamada.

Es importante tener en cuenta que no se recomienda el uso de la \[ devolución \] de llamada en la programación multiproceso. Como función de programación de un solo subproceso, no está equipada para admitir las demandas de seguridad que proporciona un entorno con varios subprocesos.

No se puede usar la función **RpcCancelThread** para cancelar una llamada que pueda enviar una devolución de llamada estática. Si una llamada a procedimiento remoto determinada nunca dará lugar a una devolución de llamada, se puede cancelar. De lo contrario, una llamada solo se puede cancelar si se puede garantizar que no se ha emitido una devolución de llamada para ella.

Solo las secuencias orientadas a la conexión y del protocolo local admiten el atributo de devolución de llamada. El tamaño de los \[ datos de salida \] para las devoluciones de llamada en la secuencia de protocolo local está limitado a 150 bytes. Si una interfaz RPC utiliza una secuencia de protocolo de conexión sin conexión, se producirá un error en las llamadas a procedimientos con el atributo de devolución de llamada.

Los identificadores no se pueden usar como parámetros en funciones de devolución de llamada. Dado que las devoluciones de llamada siempre se ejecutan en el contexto de una llamada, el identificador de enlace utilizado por el cliente para realizar la llamada al servidor también se utiliza como identificador de enlace del servidor al cliente.

Las devoluciones de llamada pueden anidar a cualquier profundidad.

## <a name="examples"></a>Ejemplos

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 