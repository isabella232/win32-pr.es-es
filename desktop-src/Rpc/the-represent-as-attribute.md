---
title: El atributo represent_as
description: El atributo \ representate \_ como \ permite especificar cómo se representa un tipo de datos transmitible determinado en la aplicación.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, atributos, represent_as llamada a procedimiento remoto
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149565"
---
# <a name="the-represent_as-attribute"></a>El atributo de representación \_ como

El \[ atributo [representate \_ as](/windows/desktop/Midl/represent-as) \] permite especificar cómo se representa un tipo de datos transmitible determinado en la aplicación. Esto se hace especificando el nombre del tipo representado para un tipo transmitible conocido y proporcionando las rutinas de conversión. También debe proporcionar las rutinas para liberar la memoria que usan los objetos de tipo de datos.

Use el atributo **\[ representar \_ como \]** para presentar una aplicación con un tipo de datos diferente, posiblemente no transmitible, en lugar del tipo que realmente se transmite entre el cliente y el servidor. También es posible que el tipo que manipula la aplicación se desconozca en el momento de la compilación de MIDL. Al elegir un tipo de transmisión bien definido, no es necesario preocuparse por la representación de datos en el entorno heterogéneo. El atributo **\[ representate \_ as \]** puede hacer que la aplicación sea más eficaz reduciendo la cantidad de datos transmitidos a través de la red.

El atributo **\[ representa \_ \] como** es similar al atributo \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] . Sin embargo, mientras se **\[ transmite \_ como \]** le permite especificar un tipo de datos que se usará para la transmisión, **\[ representa \_ como \]** le permite especificar cómo se representa un tipo de datos para la aplicación. No es necesario definir el tipo representado en los archivos procesados por MIDL; se puede definir en el momento en que se compilan los códigos auxiliares con el compilador de C. Para ello, utilice la Directiva include en el archivo de configuración de la [aplicación (ACF)](the-application-configuration-file-acf-.md) para compilar el archivo de encabezado adecuado. Por ejemplo, el siguiente ACF define un tipo local para la aplicación, **repr \_ Type**, para el tipo de transmisión **denominado \_ Type:**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

En la tabla siguiente se describen las cuatro rutinas proporcionadas por el programador.



| Rutina                      | Descripción                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **tipo con nombre \_ \_ de \_ local** | Asigna una instancia del tipo de red y convierte el tipo local al tipo de red.      |
| **tipo con nombre \_ \_ en \_ local**   | Convierte del tipo de red al tipo local.                                                    |
| **tipo con nombre \_ \_ Free \_ local** | Libera la memoria asignada por una llamada al **tipo con nombre en la rutina \_ \_ \_ local** , pero no el propio tipo. |
| **Inst. de tipo con nombre \_ \_ \_**  | Libera el almacenamiento para el tipo de red (ambos lados).                                                     |



 

Aparte de estas cuatro rutinas proporcionadas por el programador, la aplicación no manipula el tipo con nombre. El único tipo visible para la aplicación es el tipo representado. La aplicación utiliza el nombre de tipo representado en lugar del nombre de tipo transmitido en los prototipos y códigos auxiliares generados por el compilador. Debe proporcionar el conjunto de rutinas para ambos lados.

En el caso de los objetos de **\_ tipo con nombre** temporal, el código auxiliar llamará a un **tipo con nombre \_ \_ Free \_ inst** para liberar cualquier memoria asignada por una llamada a un **tipo con nombre \_ \_ de \_ local**.

Si el tipo representado es un puntero o contiene un puntero, el **tipo con nombre de la rutina \_ \_ \_ local** debe asignar la memoria para los datos a los que apuntan los punteros (el código auxiliar manipula el propio objeto de tipo representado de la manera habitual). Para \[ [los](/windows/desktop/Midl/out-idl) \] parámetros out y \[ [in](/windows/desktop/Midl/in), out \] de un tipo que contiene **\[ representan \_ como** o uno de sus componentes, se llama automáticamente a la rutina **\_ \_ \_ local de tipo con nombre** para los objetos de datos que contienen el atributo. En el caso de los parámetros **\[ in \]** , solo se llama a la rutina **\_ \_ \_ local de tipo con nombre** si el atributo **\[ representated \_ as \]** se ha aplicado al parámetro. Si el atributo se ha aplicado a los componentes del parámetro, no se llama a la rutina *\* *** \_ \_ local gratuita**. No se llama a las rutinas de liberación para los datos incrustados y la llamada más de una vez (relacionado con el atributo de nivel superior) para **\[ \] un solo parámetro** .

> [!Note]  
> Se pueden aplicar los atributos de **\[ transmisión \_ como \]** y de **\[ representación \_ \]** al mismo tipo. Al calcular las referencias de los datos, se aplica primero la conversión de tipos de **\[ representación \_ \]** y **\[ \_ \]** , a continuación, se aplica la conversión de transmisión. El orden se invierte al anular la serialización de los datos. Por lo tanto, cuando se calculan las referencias, \* **\_ desde \_ local** asigna una instancia de un tipo con nombre y la traduce de un objeto de tipo local al objeto de tipo con nombre temporal. Este objeto es el objeto de tipo presentado utilizado para la rutina de \* **\_ \_ transmisión** . A \* continuación, la rutina **\_ to de \_ transmisión** asigna un objeto de tipo transmitido y lo convierte del objeto presentado (con nombre) en el objeto transmitido.

 

Se puede utilizar una matriz de enteros Long para representar una lista vinculada. De esta manera, la aplicación manipula la lista y la transmisión utiliza una matriz de enteros largos cuando se transmite una lista de este tipo. Puede empezar con una matriz, pero el uso de una construcción con una matriz abierta de enteros largos es más conveniente. El ejemplo siguiente muestra cómo hacerlo.

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

Tenga en cuenta que los prototipos de las rutinas que usan el tipo **LONGARR** se muestran realmente en los archivos stub. h como **PLOC \_ Box** en lugar del tipo **LONGARR** . Lo mismo se aplica a los códigos auxiliares adecuados en el archivo de código auxiliar \_ c. c.

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

-   La rutina **LONGARR \_ from \_ local** cuenta los nodos de la lista, asigna un objeto LONGARR con **el tamaño sizeof (****LONGARR**) + Count \* **sizeof**(**Long**), establece el campo **size** en Count y copia los datos en el campo **DataArr** .
-   La rutina **LONGARR \_ to \_ local** crea una lista con nodos de tamaño y transfiere la matriz a los nodos correspondientes.
-   La **rutina \_ \_ inst LONGARR Free** libera nada en este caso.
-   La **rutina \_ \_ local LONGARR Free** libera todos los nodos de la lista.

 

 