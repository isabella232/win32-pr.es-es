---
title: call_as (atributo)
description: El atributo \ call as\ permite asignar una función a la que no se puede llamar de forma \_ remota a una función remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as atributo MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e91fb9bc06eb4644209d87b4a941a68bc6b4d58d4dc31010d284e7b0f959c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807378"
---
# <a name="call_as-attribute"></a>llamada \_ como atributo

La **\[ llamada \_ como \]** atributo permite asignar una función a la que no se puede llamar de forma remota a una función remota.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*local-proc* 
</dt> <dd>

Especifica una rutina definida por la operación.

</dd> <dt>

*operation-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican a la operación. Separe varios atributos con comas.

</dd> <dt>

*operation-name* 
</dt> <dd>

Especifica la operación con nombre presentada a la aplicación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La capacidad de asignar una función a la que no se puede llamar de forma remota a una función remota es especialmente útil en interfaces que tienen numerosos tipos de parámetros que no se pueden transmitir a través de la red. En lugar de usar muchos tipos de representación como y transmisión como , puede combinar todas las conversiones **\[** [**\_**](represent-as.md) mediante **\]** llamadas **\[** [**\_**](transmit-as.md) **\]** **\[ \_ \] como** rutinas. Las dos llamadas se **\[ suministran \_ como \]** rutinas (lado cliente y lado servidor) para enlazar la rutina entre las llamadas de aplicación y las llamadas remotas.

La **\[ llamada \_ como \]** atributo se puede usar para interfaces de objeto. En este caso, la definición de interfaz se puede usar para llamadas locales, **\[ \_ \]** así como para llamadas remotas, ya que la llamada a como permite que una interfaz a la que no se pueda acceder de forma remota se asigne de forma transparente a una interfaz remota. La **\[ llamada \_ como \]** atributo no se puede usar con [**el modo /osf.**](-osf.md)

Por ejemplo, suponga que la **rutina f1** en la interfaz de objeto **IFace** requiere numerosas conversiones entre las llamadas de usuario y lo que realmente se transmite. En los ejemplos siguientes se describen los archivos IDL y ACF para la **interfaz IFace**:

En el archivo IDL de la interfaz **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

En la interfaz **IFace** de ACF para :

``` syntax
[call_as( f1 )] Remf1();
```

Esto hace que el archivo de encabezado generado defina la interfaz mediante la definición de **f1,** pero también proporciona código auxiliar para **Remf1.**

El compilador MIDL generará la siguiente Vtable en el archivo de encabezado para la **interfaz IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

El proxy del lado cliente tendría entonces un proxy típico generado por MIDL para **Remf1,** mientras que el código auxiliar del lado servidor para **Remf1** sería el mismo que el código auxiliar típico generado por MIDL:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

A continuación, **\[ las dos llamadas \_ como \]** rutinas de enlace (lado cliente y lado servidor) se deben codificar manualmente:

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

En el caso de las interfaces de objetos, estos son los prototipos de las rutinas de enlace.

Para el lado cliente:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Para el lado servidor:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

En el caso de las interfaces que no son objetos, estos son los prototipos de las rutinas de enlace.

Para el lado cliente:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Para el lado servidor:

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

 

 




