---
title: El represent_as atributo
description: El atributo \ represent as\ permite especificar cómo se representa un tipo de datos \_ transmitible determinado a la aplicación.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Llamada a procedimiento remoto RPC, atributos, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361891"
---
# <a name="the-represent_as-attribute"></a>El elemento se \_ representa como atributo

El \[ [atributo representar \_ como](/windows/desktop/Midl/represent-as) le permite especificar cómo se representa un tipo de datos transmitible \] determinado a la aplicación. Para ello, se especifica el nombre del tipo representado para un tipo transmitible conocido y se suministran las rutinas de conversión. También debe proporcionar las rutinas para liberar la memoria utilizada por los objetos de tipo de datos.

Use la **\[ representación \_ como \]** atributo para presentar una aplicación con un tipo de datos diferente, posiblemente no transmitible, en lugar del tipo que se transmite realmente entre el cliente y el servidor. También es posible que el tipo que manipula la aplicación pueda ser desconocido en el momento de la compilación de MIDL. Al elegir un tipo transmitible bien definido, no es necesario preocuparse por la representación de datos en el entorno heterogéneo. El **\[ atributo representar \_ como \]** puede hacer que la aplicación sea más eficaz al reducir la cantidad de datos transmitidos a través de la red.

La **\[ representación \_ como \]** atributo es similar a \[ [la transmisión \_ como](/windows/desktop/Midl/transmit-as) \] atributo. Sin embargo, **\[ aunque la \_ \]** transmisión como permite especificar un tipo de datos que se usará para la transmisión, **\[ representar \_ \]** como le permite especificar cómo se representa un tipo de datos para la aplicación. No es necesario definir el tipo representado en los archivos procesados de MIDL; se puede definir en el momento en que los códigos auxiliares se compilan con el compilador de C. Para ello, use la directiva include en el archivo de configuración de [la aplicación (ACF)](the-application-configuration-file-acf-.md) para compilar el archivo de encabezado adecuado. Por ejemplo, el siguiente ACF define un tipo local para la aplicación, **tipo de repr \_**, para el tipo que se puede transmitir denominado **\_ type:**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

En la tabla siguiente se describen las cuatro rutinas proporcionadas por el programador.



| Rutina                      | Descripción                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **tipo \_ con nombre de \_ \_ local** | Asigna una instancia del tipo de red y convierte del tipo local al tipo de red.      |
| **tipo \_ con nombre a \_ \_ local**   | Convierte del tipo de red al tipo local.                                                    |
| **tipo \_ con nombre local \_ \_ libre** | Libera la memoria asignada por una llamada al tipo con nombre a **\_ la rutina \_ \_ local,** pero no al propio tipo. |
| **tipo \_ con nombre free \_ \_ inst**  | Libera el almacenamiento para el tipo de red (ambos lados).                                                     |



 

Aparte de estas cuatro rutinas proporcionadas por el programador, la aplicación no manipula el tipo con nombre. El único tipo visible para la aplicación es el tipo representado. La aplicación usa el nombre de tipo representado en lugar del nombre de tipo transmitido en los prototipos y códigos auxiliares generados por el compilador. Debe proporcionar el conjunto de rutinas para ambos lados.

En el caso de los objetos **\_ de** tipo con nombre temporales, el código auxiliar llamará al tipo sin nombre **\_ \_ \_ inst** para liberar cualquier memoria asignada por una llamada al tipo con nombre **de \_ \_ \_ local.**

Si el tipo representado es un puntero o contiene un puntero, el tipo con nombre a la rutina **\_ \_ \_ local** debe asignar memoria para los datos a los que apuntan los punteros (el propio objeto de tipo representado se manipula mediante el código auxiliar de la manera habitual). Para out y en , los parámetros out de un tipo que contienen representan como o uno de sus \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in) \] **\[ \_** componentes, **\_ \_ \_** se llama automáticamente a la rutina local libre de tipos con nombre para los objetos de datos que contienen el atributo . En **\[ los \]** parámetros de , se llama a la **rutina \_ \_ \_ local** libre de tipos con nombre solo si se ha aplicado el atributo **\[ representar \_ \]** como al parámetro . Si el atributo se ha aplicado a los componentes del parámetro , no se llama a la rutina * *\* *** \_ \_ local* libre. No se llama a las rutinas de liberar para los datos incrustados y la llamada al máximo una vez (relacionada con el atributo de nivel superior) para un **\[ parámetro in \]** only.

> [!Note]  
> Es posible aplicar la transmisión **\[ \_ \] como** y **\[ representar \_ \] como** atributos al mismo tipo. Al serializar los datos, primero se **\[ \_ aplica \] la** conversión de la representación como tipo y, a **\[ \_ \]** continuación, se aplica la conversión de transmisión como. El orden se invierte al desmarque de datos. Por lo tanto, al serializar, desde local asigna una instancia de un tipo con nombre y la convierte de un objeto de tipo local al objeto de tipo con nombre \* *_\_ \__* temporal. Este objeto es el objeto de tipo presentado que se usa para la \* *_\_ rutina \_ to xmit._* A \* *_\_ \_ continuación, la_* rutina to xmit asigna un objeto de tipo transmitido y lo traduce del objeto presentado (con nombre) al objeto transmitido.

 

Se puede usar una matriz de enteros largos para representar una lista vinculada. De esta manera, la aplicación manipula la lista y la transmisión usa una matriz de enteros largos cuando se transmite una lista de este tipo. Puede comenzar con una matriz, pero es más conveniente usar una construcción con una matriz abierta de enteros largos. El ejemplo siguiente muestra cómo hacerlo.

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

Tenga en cuenta que los prototipos de las rutinas que usan el tipo **LONGARR** se muestran realmente en los archivos Stub.h como **PLOC \_ BOX** en lugar del tipo **LONGARR.** Lo mismo sucede con los códigos auxiliares adecuados en el \_ archivo C.c de código auxiliar.

Debe proporcionar las cuatro funciones siguientes:

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

Las rutinas mostradas anteriormente hacen lo siguiente:

-   LongARR de la rutina **\_ \_ local** cuenta los nodos de la lista, asigna un objeto LONGARR con el tamaño **sizeof**(**LONGARR**) + Count sizeof ( long ), establece el campo Tamaño en Recuento y copia los datos en el \* ** **campo DataArr.**  
-   La **rutina LONGARR \_ a \_ local** crea una lista con nodos Size y transfiere la matriz a los nodos adecuados.
-   En este caso, la rutina **free \_ \_ inst de LONGARR** no libera nada.
-   La rutina local gratuita **\_ \_ LONGARR** libera todos los nodos de la lista.

 

 