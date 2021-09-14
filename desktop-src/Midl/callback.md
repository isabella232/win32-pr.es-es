---
title: Atributo de devolución de llamada
description: El atributo \ callback\ declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida. Las funciones de devolución de llamada proporcionan una manera de que el servidor ejecute código en el cliente.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- MidL del atributo de devolución de llamada
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159654"
---
# <a name="callback-attribute"></a>Atributo de devolución de llamada

El **\[ atributo \] de devolución** de llamada declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida. Las funciones de devolución de llamada proporcionan una manera de que el servidor ejecute código en el cliente.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-attr-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son locales; el atributo de puntero **\[** [](local.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo base , [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type o type identifier. [ \_](midl-base-types.md) Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*ptr-declarator* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> <dt>

*declarador* 
</dt> <dd>

Especifica un declarador de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). El identificador de nombre de parámetro es opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\[ función \] de devolución** de llamada es útil cuando el servidor debe obtener información del cliente. Si las aplicaciones de servidor se admiten en Windows 3. *x*, el servidor podría realizar una llamada a un procedimiento remoto en el Windows 3. *x* server para obtener la información necesaria. La función de devolución de llamada realiza el mismo propósito y permite al servidor consultar al cliente para obtener información en el contexto de la llamada original.

Las devoluciones de llamada son casos especiales de llamadas remotas que se ejecutan como parte de un único subproceso. Se emite una devolución de llamada en el contexto de una llamada remota. Cualquier procedimiento remoto definido como parte de la misma interfaz que la función de devolución de llamada estática puede llamar a la función de devolución de llamada.

Es importante tener en cuenta que no se recomienda el uso de la devolución de \[ llamada en la \] programación multiproceso. Como función de programación de un solo subproceso, no está equipado para admitir las demandas de seguridad que proporciona un entorno de varios subprocesos.

La **función RpcCancelThread** no se puede usar para cancelar una llamada que pueda enviar una devolución de llamada estática. Si una llamada a procedimiento remoto determinada nunca dará como resultado una devolución de llamada, se puede cancelar. De lo contrario, solo se puede cancelar una llamada si se puede garantizar que no se ha emitido una devolución de llamada para ella.

Solo las secuencias de protocolo local y orientadas a la conexión admiten el atributo de devolución de llamada. El tamaño de los datos de salida para las devoluciones de llamada a través de la \[ secuencia de protocolo local está limitado a \] 150 bytes. Si una interfaz RPC usa una secuencia de protocolo sin conexión (datagrama), se producirá un error en las llamadas a procedimientos con el atributo de devolución de llamada.

Los identificadores no se pueden usar como parámetros en las funciones de devolución de llamada. Dado que las devoluciones de llamada siempre se ejecutan en el contexto de una llamada, el identificador de enlace utilizado por el cliente para realizar la llamada al servidor también se usa como identificador de enlace del servidor al cliente.

Las devoluciones de llamada se pueden anidar en cualquier profundidad.

## <a name="examples"></a>Ejemplos

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 