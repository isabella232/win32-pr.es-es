---
title: Descriptor de encabezado de procedimiento
description: El encabezado se ha ampliado varias veces a lo largo de la vida del motor de NDR. El compilador actual todavía genera encabezados diferentes en función del modo del compilador. Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488114"
---
# <a name="procedure-header-descriptor"></a>Descriptor de encabezado de procedimiento

El encabezado se ha ampliado varias veces a lo largo de la vida del motor de NDR. El compilador actual todavía genera encabezados diferentes en función del modo del compilador. Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.

## <a name="the-old-oi-header"></a>El encabezado-OI anterior

El encabezado tiene el formato siguiente:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Donde \_ el tipo de identificador<1> puede ser uno de los valores que se muestran en la tabla siguiente.



| Hex | Handle               |
|-----|----------------------|
| 31  | \_genérico de enlace de FC \_    |
| 32  | \_primitiva de enlace FC \_  |
| 33  | \_controlador automático de FC \_     |
| 34  | \_identificador de devolución de llamada FC \_ |
| 0   | (identificador explícito)    |



 

Si el tipo de identificador \_<1> campo es distinto de cero, el procedimiento utiliza un identificador implícito del tipo indicado. Vea el tema sobre [identificadores](handles.md) para obtener más información. Si el tipo de identificador \_<1> campo es cero, el identificador usado para el enlace es uno de los parámetros del procedimiento.

Los identificadores explícitos pueden ser primitivos, genéricos y de contexto; el último tiene el siguiente token de FC.



| Hex | Handle            |
|-----|-------------------|
| 30  | \_contexto de enlace FC \_ |



 

Por Convención, el tipo de identificador de las interfaces DCOM es el \_ identificador automático de FC \_ .

Las \_ marcas Oi<1> campo es una máscara de 8 bits de las marcas siguientes.



| Hex | Marca                         | Significado                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Se \_ \_ usó el PTR completo de OI \_          | Utiliza el paquete de puntero completo.           |
| 02  | \_Asignación RPCSS de OI \_ \_ usada       | Utiliza el paquete de memoria RpcSs.           |
| 04  | \_Procedimiento de objeto OI \_             | Un procedimiento en una interfaz de objeto.      |
| 08  | OI \_ tiene \_ RPCFLAGS            | El procedimiento tiene marcas RPC que no son cero.     |
| 10  | OI\_\*                       | Sobrecargado.                              |
| 20  | OI\_\*                       | Sobrecargado.                              |
| 40  | OI \_ usar \_ nuevas \_ rutinas de inicialización \_ | Utiliza las rutinas de Windows NT 3.5 beta2 + init. |
| 80  |                              | Sin usar.                                  |



 

Las marcas siguientes se sobrecargan.



| Hex | Marca                                    | Significado                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | \_se utiliza ENcode \_                        | Solo se usa en la selección.                              |
| 20  | descodificación \_ se \_ usa                        | Solo se usa en la selección.                              |
| 10  | \_Omitir \_ el \_ control de excepciones de objeto \_ | Ya no se utiliza (OLE anterior).                         |
| 20  | OI \_ tiene \_ COMM \_ o \_ error                | Solo en RPC sin formato, \[ COMM \_ , \_ Estado de error \] .        |
| 20  | La OI ( \_ obj) \_ use el \_ \_ intérprete V2           | Solo en DCOM, use el intérprete [**-saliente**](/windows/desktop/Midl/-oi) . |



 

El \_ campo marcas de rpc<4> describe cómo establecer el campo **RpcFlags** de la estructura de [**\_ mensajes RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) . Este campo solo está presente si las \_ marcas oi<1> campo tiene OI \_ \_ RPCFLAGS establecido. Si este campo no está presente, las marcas de RPC para el procedimiento remoto son cero.

> [!Note]  
> Para el rendimiento, los intérpretes asincrónicos siempre tienen las \_ marcas rpc<4> campo presente.

 

El \_ campo de> proc num<2 proporciona el número de procedimiento del procedimiento.

El \_ tamaño de la pila<2> proporciona el tamaño total de todos los parámetros de la pila, incluido este puntero o valor devuelto.

La \_ Descripción del identificador explícito \_<> campo se describe más adelante en este documento. Este campo no está presente si el procedimiento usa un identificador implícito.

 

 