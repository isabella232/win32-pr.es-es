---
title: call_as (atributo)
description: El atributo \ Call \_ as \ permite asignar una función a la que no se puede llamar de forma remota a una función remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as el atributo MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651338"
---
# <a name="call_as-attribute"></a>llamar a \_ como atributo

El atributo **\[ Call \_ as \]** permite asignar una función a la que no se puede llamar de forma remota a una función remota.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*procedimiento local* 
</dt> <dd>

Especifica una rutina definida por la operación.

</dd> <dt>

*operación-atributo-lista* 
</dt> <dd>

Especifica uno o más atributos que se aplican a la operación. Separe varios atributos con comas.

</dd> <dt>

*nombre de operación* 
</dt> <dd>

Especifica la operación con nombre que se presenta a la aplicación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La capacidad de asignar una función a la que no se puede llamar de forma remota a una función remota es especialmente útil en las interfaces que tienen numerosos tipos de parámetro que no se pueden transmitir a través de la red. En lugar de usar muchos **\[** [**representan \_ como**](represent-as.md) **\]** y **\[** [**transmitir \_ como**](transmit-as.md) **\]** tipos, puede combinar todas las conversiones mediante las rutinas **\[ Call \_ as \]** . Proporcione las dos **\[ llamadas \_ como \]** rutinas (lado cliente y servidor) para enlazar la rutina entre las llamadas a la aplicación y las llamadas remotas.

El atributo **\[ Call \_ as \]** se puede usar para las interfaces de objeto. En este caso, la definición de la interfaz se puede usar para las llamadas locales, así como para las llamadas remotas, ya que la **\[ llamada \_ as \]** permite que una interfaz a la que no se puede tener acceso de forma remota se asigne de manera transparente a una interfaz remota. El atributo **\[ Call \_ as \]** no se puede usar con el modo [**/OSF**](-osf.md) .

Por ejemplo, supongamos que la rutina **F1** en la interfaz de objeto **IFace** requiere numerosas conversiones entre las llamadas del usuario y lo que realmente se transmite. En los ejemplos siguientes se describen los archivos IDL y ACF de la interfaz **IFace**:

En el archivo IDL de la interfaz **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

En ACF para la interfaz **IFace**:

``` syntax
[call_as( f1 )] Remf1();
```

Esto hace que el archivo de encabezado generado defina la interfaz utilizando la definición de **F1**, pero también proporciona códigos auxiliares para **Remf1**.

El compilador MIDL generará la siguiente tabla vtable en el archivo de encabezado de la interfaz **IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

Después, el proxy del lado cliente tendría un proxy generado por MIDL típico para **Remf1**, mientras que el código auxiliar del lado servidor para **Remf1** sería el mismo que el código auxiliar típico generado por MIDL:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

A continuación, se deben codificar manualmente las dos **\[ llamadas \_ como \]** rutinas de enlace (lado cliente y servidor):

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

En el caso de las interfaces de objeto, estos son los prototipos para las rutinas de enlace.

Para el lado cliente:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

En el lado del servidor:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

En el caso de las interfaces que no son de objeto, estos son los prototipos de las rutinas de Bond.

Para el lado cliente:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

En el lado del servidor:

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> </dl>

 

 




