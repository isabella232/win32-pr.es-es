---
title: Punteros (RPC)
description: Obtenga información sobre un puntero común RPC, que se define como todo lo que no sea punteros de interfaz y punteros de recuento de bytes.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a87c13f9657d56e3f85d1d5828dc097c25e29990c617c5f20679a1d6cbe91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927355"
---
# <a name="pointers-rpc"></a>Punteros (RPC)

## <a name="common-pointers"></a>Punteros comunes

Un puntero común se define como todo lo que no sea punteros de interfaz y punteros de recuento de bytes.

Hay dos diseños posibles para la descripción:

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

-o bien-

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

El primer formato se usa si el puntero es un puntero a un tipo simple o a un puntero de cadena no especificado. El segundo formato se usa para punteros a todos los demás tipos. Los atributos de puntero indican qué diseño de descripción tiene la marca \_ FC SIMPLE \_ POINTER.

el \_ tipo de<1> es uno de los siguientes.



| Carácter de formato | Descripción                              |
|------------------|------------------------------------------|
| FC \_ RP           | Puntero de referencia.                     |
| FC \_ UP           | Puntero único.                        |
| FC \_ FP           | Puntero completo.                          |
| FC \_ OP           | Puntero único en una interfaz de objeto. |



 

La razón para distinguir FC OP es semántica: en las interfaces de objeto, se debe liberar un puntero in-out antes de desmarque un nuevo objeto y asignar un nuevo valor \_ \[ de \] puntero.

Los atributos<1> pueden tener cualquiera de las marcas \_ que se muestran en la tabla siguiente.



| Atributo | Marca              | Descripción                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ ASIGNA TODOS LOS \_ \_ NODOS | El puntero forma parte de un esquema de asignación allocate(all \_ nodes).                                                                                                                                                                   |
| 02   | FC \_ DONT \_ FREE           | Puntero allocate(don't \_ free).                                                                                                                                                                                                      |
| 04   | FC \_ ALLOCED \_ ON \_ STACK   | Puntero cuyo referencia se asigna en la pila del código auxiliar.                                                                                                                                                                            |
| 08   | PUNTERO \_ SIMPLE DE \_ FC      | Puntero a un tipo simple o cadena compatible no compatible. Esta marca que se establece indica el diseño de la descripción del puntero como el diseño de puntero simple descrito anteriormente; de lo contrario, se indica el formato del descriptor con el desplazamiento. |
| 10   | FC \_ POINTER \_ DEREF       | Puntero que se debe desreferenciar antes de controlar el referenciador del puntero.                                                                                                                                                           |



 

Los punteros que tienen size \_ is(), max \_ is(), length \_ is(), last \_ is() o first \_ is() aplicados \_ \_ \_ tienen descripciones de cadenas de formato idénticas a un puntero a una matriz del tipo adecuado (por ejemplo, una matriz compatible si size is() se aplica, una matriz variable conforme si size is() y length se aplica).

## <a name="interface-pointers"></a>Punteros de interfaz

Una cadena de formato de puntero de interfaz de objeto tiene uno de dos formatos, dependiendo de si el compilador conoce el IID correspondiente.

Un puntero de interfaz con un IID constante tiene la descripción siguiente:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

El valor de<16> es el IID real del puntero de interfaz. El iid se escribe en la cadena de formato en un formato idéntico a la estructura de datos GUID: long, short, short, char \[ 8 \] .

La descripción de un puntero de interfaz con \_ iid is() aplicado a él es:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

La descripción de iid<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ si [**se usa /robust.**](/windows/desktop/Midl/-robust) El valor calculado por **la función ComputeConformance** es el puntero IID.

## <a name="byte-count-pointers"></a>Punteros de recuento de bytes

Los punteros de recuento de bytes se relacionan con un atributo de optimización especial denominado \[ **recuento de \_ bytes.** \] Se usan los siguientes formatos:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

–y –

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

La descripción del recuento<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ \_ si se usa [**/robust.**](/windows/desktop/Midl/-robust)

La descripción \_ de<> es una descripción del tipo de objeto .

 

 
