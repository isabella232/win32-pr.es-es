---
title: El atributo transmit_as
description: El atributo \ Transmit \_ as ofrece una manera de controlar el cálculo de referencias de datos sin preocuparse por la serialización de datos en un nivel bajo \ 8212; es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno heterogéneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, atributos, transmit_as llamada a procedimiento remoto
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421110"
---
# <a name="the-transmit_as-attribute"></a>Atributo de transmisión \_ como

El **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** ofrece una manera de controlar el cálculo de referencias de datos sin preocuparse por la serialización de datos en un nivel bajo, es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno heterogéneo. Al permitirle reducir la cantidad de datos que se transmiten a través de la red, el atributo **\[ transmitir \_ como \]** puede hacer que la aplicación sea más eficaz.

El atributo **\[ transmitir \_ como \]** se usa para especificar un tipo de datos que el código auxiliar de RPC transmitirá a través de la red en lugar de usar el tipo de datos proporcionado por la aplicación. Se proporcionan rutinas que convierten el tipo de datos a y del tipo que se utiliza para la transmisión. También debe proporcionar rutinas para liberar la memoria que se usa para el tipo de datos y el tipo transmitido. Por ejemplo, a continuación se define el **\_ tipo de transmisión** como el tipo de datos transmitido para todos los datos de aplicación especificados como de tipo **\_ espec**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

En la tabla siguiente se describen los cuatro nombres de rutinas proporcionados por el programador. **Type** es el tipo de datos que la aplicación conoce y **\_ tipo de transmisión** es el tipo de datos que se usa para la transmisión.



| Rutina                                                 | Descripción                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo \_ que se va a \_ transmisión**](the-type-to-xmit-function.md)     | Asigna un objeto del tipo transmitido y convierte de tipo de aplicación al tipo transmitido a través de la red (llamador y objeto llamado). |
| [**Tipo \_ de \_ transmisión**](the-type-from-xmit-function.md) | Convierte del tipo transmitido al tipo de aplicación (llamador y objeto llamado).                                                                  |
| [**Tipo \_ \_ inst gratis**](the-type-free-inst-function.md) | Libera los recursos utilizados por el tipo de aplicación (solo denominado objeto).                                                                              |
| [**\_Transmisión libre de tipos \_**](the-type-free-xmit-function.md) | Libera el almacenamiento devuelto por el tipo para la rutina de *****\_*** \_ transmisión** (llamador y el objeto denominado).                                                      |



 

Aparte de estas cuatro funciones proporcionadas por el programador, la aplicación no manipula el tipo transmitido. El tipo transmitido solo se define para trasladar datos a través de la red. Una vez que los datos se han convertido al tipo utilizado por la aplicación, se libera la memoria utilizada por el tipo transmitido.

Estas rutinas proporcionadas por el programador las proporciona el cliente o la aplicación de servidor en función de los atributos direccionales. Si el parámetro es **\[** solo [**en**](/windows/desktop/Midl/in) **\]** , el cliente se transmite al servidor. El cliente necesita el **tipo \_ para la \_ transmisión** y el tipo de las funciones de **\_ \_ transmisión libres** . El servidor necesita el **tipo \_ de \_** las funciones de tipo de la transmisión y **\_ liberación de \_ inst** . Para un **\[** [](/windows/desktop/Midl/out-idl) **\]** parámetro de solo salida, el servidor se transmite al cliente. La aplicación de servidor debe implementar el **tipo \_ para la \_ transmisión** y el tipo de las funciones de **\_ \_ transmisión libres** , mientras que el programa cliente debe proporcionar el **tipo de la función \_ de \_ transmisión** . En el caso de los objetos de **\_ tipo de transmisión** temporales, el código auxiliar llamará a la *****\_*** \_ transmisión libre de tipos** para liberar cualquier memoria asignada por una llamada al **tipo para la \_ \_ transmisión**.

Ciertas directrices se aplican a la instancia de tipo de aplicación. Si el tipo de aplicación es un puntero o contiene un puntero, el **tipo** \_ **de la rutina de \_ transmisión** debe asignar memoria para los datos a los que apuntan los punteros (el código auxiliar manipula el objeto de tipo de aplicación de la manera habitual).

En el **caso de los parámetros out y \[ in, out o uno de sus componentes, de un tipo que contiene el atributo Transmit as, se llama automáticamente a la rutina inst Free de tipo para los objetos de datos que tienen el atributo. \]** **\[ \] \]** **\[ \_ \]**  \_ **\_** En el caso de los parámetros **in** ,  \_ se llama a la rutina **\_ inst inst** de tipo solo si se ha aplicado el atributo de **\[ transmisión \_ como \]** al parámetro. Si el atributo se ha aplicado a los componentes del parámetro,  \_ no se llama a la rutina **\_ inst Free** de tipo. No hay ninguna llamada de liberación para los datos incrustados y, a lo sumo, una llamada (relacionada con el atributo de nivel superior) **para un solo** parámetro.

Con MIDL 2,0, tanto el cliente como el servidor deben proporcionar las cuatro funciones. Por ejemplo, una lista vinculada se puede transmitir como una matriz de tamaño. El **tipo \_ para \_** la rutina de transmisión recorre la lista vinculada y copia los datos ordenados en una matriz. Los elementos de la matriz se ordenan de modo que no es necesario transmitir los muchos punteros asociados a la estructura de lista. El **tipo \_ de la rutina de \_ transmisión** lee la matriz y coloca sus elementos en una estructura de lista vinculada.

La lista vinculada doble ( \_ lista de vínculos dobles \_ ) incluye datos y punteros a los elementos de la lista anterior y siguiente:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

En lugar de enviar la estructura compleja, el **\[** atributo [**Transmit \_ as**](/windows/desktop/Midl/transmit-as) **\]** se puede usar para enviarlo a través de la red como una matriz. La secuencia de elementos de la matriz conserva el orden de los elementos de la lista a un costo más bajo:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

El atributo **\[ transmitir \_ como \]** aparece en el archivo IDL:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

En el ejemplo siguiente, **ModifyListProc** define el parámetro de tipo Double \_ Link \_ Type como **\[ in, \] out** Parameter:

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Las cuatro funciones definidas por el programador usan el nombre del tipo en los nombres de función y usan los tipos presentados y transmitidos como tipos de parámetro, según sea necesario:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 