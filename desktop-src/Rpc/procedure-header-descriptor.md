---
title: Descriptor de encabezado de procedimiento
description: El encabezado se ha extendido varias veces a lo largo de la vida del motor REACTOR. El compilador actual sigue generando encabezados diferentes en función del modo del compilador. Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd9572c9a29ea8477f1d06d8786d50f6abf920de140b6d1663c2431b2ad0c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927143"
---
# <a name="procedure-header-descriptor"></a>Descriptor de encabezado de procedimiento

El encabezado se ha extendido varias veces a lo largo de la vida del motor REACTOR. El compilador actual sigue generando encabezados diferentes en función del modo del compilador. Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.

## <a name="the-old-oi-header"></a>Encabezado –Oi anterior

El encabezado tiene el formato siguiente:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Donde el \_ tipo de<1> puede ser uno de los valores que se muestran en la tabla siguiente.



| Hex | Handle               |
|-----|----------------------|
| 31  | FC \_ BIND \_ GENERIC    |
| 32  | PRIMITIVA \_ DE ENLACE DE \_ FC  |
| 33  | CONTROLADOR \_ AUTOMÁTICO DE \_ FC     |
| 34  | IDENTIFICADOR DE \_ DEVOLUCIÓN DE LLAMADA DE \_ FC |
| 0   | (identificador explícito)    |



 

Si el tipo de<campo 1> es distinto de cero, el procedimiento usa un identificador implícito \_ del tipo indicado. Vea el [tema Handles](handles.md) (Identificadores) para obtener más información. Si el tipo de<1> campo es cero, el identificador utilizado para el enlace es uno de \_ los parámetros del procedimiento.

Los identificadores explícitos pueden ser primitivos, genéricos y contexto; el último tiene el siguiente token de FC.



| Hex | Handle            |
|-----|-------------------|
| 30  | CONTEXTO \_ DE ENLACE DE \_ FC |



 

Por convención, el tipo de identificador para las interfaces DCOM es FC \_ AUTO \_ HANDLE.

Las marcas de IA<campo 1> es una máscara de \_ 8 bits de las marcas siguientes.



| Hex | Marca                         | Significado                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ FULL \_ PTR \_ USED          | Usa el paquete de puntero completo.           |
| 02  | Oi \_ RPCSS \_ ALLOC \_ USED       | Usa el paquete de memoria RpcSs.           |
| 04  | Oi \_ OBJECT \_ PROC             | Procedimiento en una interfaz de objeto.      |
| 08  | Oi \_ TIENE \_ RPCFLAGS            | El procedimiento tiene marcas Rpc distintas de cero.     |
| 10  | Oi\_\*                       | Sobrecargado.                              |
| 20  | Oi\_\*                       | Sobrecargado.                              |
| 40  | OI \_ USE \_ NUEVAS \_ RUTINAS DE INIT \_ | Usa Windows rutinas de init NT3.5 Beta2+. |
| 80  |                              | Sin usar.                                  |



 

Las marcas siguientes están sobrecargadas.



| Hex | Marca                                    | Significado                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | SE USA \_ LA \_ CODIFICACIÓN                        | Solo se usa en el pickling.                              |
| 20  | SE USA \_ \_ DESCODIFICACIÓN                        | Solo se usa en el pickling.                              |
| 10  | Oi \_ IGNORE \_ OBJECT \_ EXCEPTION \_ HANDLING | Ya no se usa (OLE antiguo).                         |
| 20  | Oi \_ TIENE \_ COMM O \_ \_ ERROR                | Solo en RPC sin formato, \[ comm \_ , estado de \_ error \] .        |
| 20  | Oi \_ OBJ \_ USE \_ V2 \_ INTERPRETER           | Solo en DCOM, use [**el intérprete –Oif.**](/windows/desktop/Midl/-oi) |



 

Las marcas rpc<campo 4> describe cómo establecer el \_ **campo RpcFlags** de la [**estructura RPC \_ MESSAGE.**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) Este campo solo está presente si las marcas de Oi<1> campo \_ tiene Oi \_ HAD \_ RPCFLAGS establecido. Si este campo no está presente, las marcas RPC del procedimiento remoto son cero.

> [!Note]  
> Para mejorar el rendimiento, los intérpretes asincrónicos siempre tienen presentes las \_ marcas rpc<4> campo.

 

El campo \_ proc num<2> proporciona el número de procedimiento del procedimiento.

El tamaño de pila<2> proporciona el tamaño total de todos los parámetros de la pila, incluido cualquier valor devuelto o \_ puntero.

La descripción \_ explícita del identificador<> campo se describe más adelante en este \_ documento. Este campo no está presente si el procedimiento usa un identificador implícito.

 

 