---
title: El transmit_as atributo
description: El atributo \ transmit as\ ofrece una manera de controlar la serialización de datos sin preocuparse de serializar datos en un nivel bajo \ 8212; es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno \_ heterogéneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Llamada a procedimiento remoto RPC, atributos, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617422c50bae46de72bac1e548b6f248b19d0cb2436ac0c08b265bbba4f5a6cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016645"
---
# <a name="the-transmit_as-attribute"></a>Transmitir \_ como atributo

El atributo de transmisión como ofrece una manera de controlar la serialización de datos sin preocuparse por serializar datos en un nivel bajo, es decir, sin preocuparse por los tamaños de datos o el intercambio de bytes en un entorno **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** heterogéneo. Al permitirle reducir la cantidad de datos transmitidos a través de la red, el atributo **\[ transmitir \_ como \]** puede hacer que la aplicación sea más eficaz.

Use la **transmisión \[ \_ \]** como atributo para especificar un tipo de datos que los códigos auxiliares rpc transmitirán a través de la red en lugar de usar el tipo de datos proporcionado por la aplicación. Se suministran rutinas que convierten el tipo de datos en y desde el tipo que se usa para la transmisión. También debe proporcionar rutinas para liberar la memoria usada para el tipo de datos y el tipo transmitido. Por ejemplo, a continuación se define el tipo **xmit \_** como el tipo de datos transmitido para todos los datos de aplicación especificados como de **especificación de \_ tipo**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el programador. **Type** es el tipo de datos conocido por la aplicación y **el tipo xmit \_** es el tipo de datos utilizado para la transmisión.



| Rutina                                                 | Descripción                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**type \_ to \_ xmit**](the-type-to-xmit-function.md)     | Asigna un objeto del tipo transmitido y convierte del tipo de aplicación al tipo transmitido a través de la red (llamador y objeto llamado). |
| [**Tipo \_ de \_ xmit**](the-type-from-xmit-function.md) | Convierte del tipo transmitido al tipo de aplicación (llamador y objeto llamado).                                                                  |
| [**Escriba \_ \_ free inst**](the-type-free-inst-function.md) | Libera los recursos usados por el tipo de aplicación (objeto al que solo se llama).                                                                              |
| [**Escriba \_ \_ xmit gratis.**](the-type-free-xmit-function.md) | Libera el almacenamiento devuelto por el tipo **para** _\__ *_la rutina \_ xmit_* (llamador y objeto llamado).                                                      |



 

Aparte de estas cuatro funciones proporcionadas por el programador, la aplicación no manipula el tipo transmitido. El tipo transmitido solo se define para mover datos a través de la red. Una vez que los datos se convierten al tipo utilizado por la aplicación, se libera la memoria utilizada por el tipo transmitido.

El cliente o la aplicación de servidor proporcionan estas rutinas proporcionadas por el programador en función de los atributos direccionales. Si el parámetro solo **\[** [**está en**](/windows/desktop/Midl/in) **\]** , el cliente transmite al servidor. El cliente necesita el **tipo para \_ \_ xmit y** escribir funciones **\_ \_ xmit** gratuitas. El servidor necesita el **tipo de las funciones \_ \_ xmit** **y free \_ \_ inst.** Para un **\[** [**parámetro**](/windows/desktop/Midl/out-idl) **\]** de solo salida, el servidor transmite al cliente. La aplicación de servidor debe implementar el tipo para las funciones **\_ \_ xmit** y **free \_ \_ xmit,** mientras que el programa cliente debe proporcionar el tipo **de la función \_ \_ xmit.** Para los objetos **de tipo xmit \_** temporales, el código auxiliar llamará al tipo  _\__ *_\_ free xmit_* para liberar cualquier memoria asignada por una llamada al tipo **para \_ \_ xmit**.

Ciertas directrices se aplican a la instancia de tipo de aplicación. Si el tipo de aplicación es un puntero o contiene un puntero, el tipo de la rutina \_ **\_ xmit** debe asignar memoria para los datos a los que apuntan los punteros (el propio objeto de tipo de aplicación se manipula mediante el código auxiliar de la manera habitual).

Para los parámetros **\[ out \]** y **\[ in, \] \]** out o uno de sus componentes, de un tipo que contiene la transmisión como **\[ \_ \] atributo,** se llama automáticamente a la rutina de entrada libre de tipos para los objetos de datos que tienen el \_ **\_** atributo . En **los** parámetros de , se **llama a la** rutina \_ **\_ inst** libre de tipos solo si el atributo **\[ transmitir \_ como \]** se ha aplicado al parámetro . Si el atributo se ha aplicado a los componentes del parámetro , no se llama a la rutina \_ **\_ inst** libre de tipos. No hay llamadas de liberación para los datos incrustados y como máximo una llamada (relacionada con el atributo de nivel superior) para un **parámetro in** only.

A partir de MIDL 2.0, tanto el cliente como el servidor deben proporcionar las cuatro funciones. Por ejemplo, una lista vinculada se puede transmitir como una matriz de tamaño. El **tipo de rutina \_ \_ xmit** recorre la lista vinculada y copia los datos ordenados en una matriz. Los elementos de matriz se ordenan para que no sea necesario transmitir los muchos punteros asociados a la estructura de lista. El **tipo de la rutina \_ \_ xmit** lee la matriz y coloca sus elementos en una estructura de lista vinculada.

La lista de vínculos dobles (DOUBLE LINK LIST) incluye datos y punteros a \_ los elementos de lista anterior y \_ siguiente:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

En lugar de enviar la estructura compleja, el atributo transmitir como se puede usar para enviarlo a través de la red como una **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** matriz. La secuencia de elementos de la matriz conserva el orden de los elementos de la lista a un costo menor:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

El **\[ atributo transmitir \_ como \]** aparece en el archivo IDL:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

En el ejemplo siguiente, **ModifyListProc** define el parámetro de tipo DOUBLE \_ LINK TYPE como un parámetro de entrada \_ **\[ y \]** salida:

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

 

 