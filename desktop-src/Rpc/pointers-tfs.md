---
title: Punteros (RPC)
description: Punteros
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149779"
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

El primer formato se utiliza si el puntero es un puntero a un tipo simple o un puntero de cadena sin tamaño. El segundo formato se utiliza para punteros a todos los demás tipos. Los atributos de puntero indican qué diseño de la descripción es con la \_ marca de puntero simple de FC \_ .

\_el tipo de puntero<1> es uno de los siguientes.



| Carácter de formato | Descripción                              |
|------------------|------------------------------------------|
| RP de FC \_           | Puntero de referencia.                     |
| FC \_ up           | Un puntero único.                        |
| FP de FC \_           | Puntero completo.                          |
| OP de FC \_           | Un puntero único en una interfaz de objeto. |



 

La razón para distinguir FC \_ op es semántica: en las interfaces de objeto, \[ \] se debe liberar un puntero in, out antes de quitar las referencias a un nuevo objeto y asignar un nuevo valor de puntero.

Los \_ atributos de puntero<1> pueden tener cualquiera de las marcas que se muestran en la tabla siguiente.



| Marca | Descripción              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | \_asignación de \_ todos los \_ nodos de FC | El puntero es una parte de un esquema de asignación de asignación (todos los \_ nodos).                                                                                                                                                                   |
| 02   | FC \_ \_ sin disponibilidad           | Puntero de asignación (no \_ disponible).                                                                                                                                                                                                      |
| 04   | \_ALLOCED \_ de FC en la \_ pila   | Puntero cuyo referente se asigna en la pila del código auxiliar.                                                                                                                                                                            |
| 08   | \_puntero simple \_ FC      | Un puntero a un tipo simple o una cadena compatible sin tamaño. Esta marca se establece indica el diseño de la descripción del puntero como el diseño de puntero simple descrito anteriormente; de lo contrario, se indica el formato de descriptor con el desplazamiento. |
| 10   | \_puntero FC \_ deref       | Puntero al que se debe desreferenciar antes de controlar el referente del puntero.                                                                                                                                                           |



 

Los punteros cuyo tamaño \_ es (), Max \_ is (), length \_ is (), Last \_ is (), y/o First \_ is () aplicados que tienen descripciones de cadena de formato idénticas a un puntero a una matriz del tipo apropiado (por ejemplo, una matriz compatible Si se \_ aplica size (), se aplica una matriz de variación compatible Si el tamaño \_ es () y se aplica la longitud \_ .

## <a name="interface-pointers"></a>Punteros de interfaz

Una cadena de formato de puntero de interfaz de objeto tiene uno de dos formatos, dependiendo de si el compilador conoce el IID correspondiente.

Un puntero de interfaz con un IID constante tiene la siguiente descripción:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

El IID<16> parte es el IID real para el puntero de interfaz. El IID se escribe en la cadena de formato en un formato idéntico al de la estructura de datos GUID: Long, Short, Short, Char \[ 8 \] .

La descripción de un puntero de interfaz con IID \_ es () aplicada:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

La descripción del IID \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) . El valor calculado por la función **NdrComputeConformance** es el puntero IID.

## <a name="byte-count-pointers"></a>Punteros de recuento de bytes

Los punteros de recuento de bytes están relacionados con un atributo de optimización especial denominado \[ **\_ recuento de bytes** \] . Se utilizan los siguientes formatos:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

etc

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

La descripción del recuento de bytes \_ \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .

La descripción del puntero \_<> es una descripción del tipo de puntero.

 

 
