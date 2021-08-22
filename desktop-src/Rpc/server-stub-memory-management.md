---
title: Administración de memoria de código auxiliar del servidor
description: Administración de memoria de código auxiliar del servidor
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Administración de memoria de código auxiliar del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c772678e28a51c4d5162472bc7b0ef73e19888feefbd0e1890cb13f65650425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925192"
---
# <a name="server-stub-memory-management"></a>Administración de memoria de código auxiliar del servidor

## <a name="an-introduction-to-server-stub-memory-management"></a>Introducción a la administración Server-Stub memoria

Los códigos auxiliares generados por MIDL actúan como la interfaz entre un proceso de cliente y un proceso de servidor. Un código auxiliar de cliente serializa todos los datos pasados a parámetros marcados con el atributo [**\[ in \]**](../midl/in.md) y los envía al código auxiliar del servidor. El código auxiliar del servidor, al recibir estos datos, reconstruye la pila de llamadas y, a continuación, ejecuta la función de servidor implementada por el usuario correspondiente. El código auxiliar del servidor también serializa los datos de parámetro marcados con el atributo [**\[ out \]**](../midl/out-idl.md) y los devuelve a la aplicación cliente.

El formato de datos serializados de 32 bits usado por MSRPC es una versión compatible de la sintaxis de transferencia de representación de datos de red ( HIPAA). Para obtener más información sobre este formato, consulte [el sitio web de Open Group](https://www.opengroup.org/). En el caso de las plataformas de 64 bits, se puede usar una extensión de Microsoft de 64 bits para la sintaxis de transferencia de QL denominada UNIX64 para mejorar el rendimiento.

## <a name="unmarshaling-inbound-data"></a>Desmarque los datos entrantes

En MSRPC, el código auxiliar del cliente [**\[ \]**](../midl/in.md) serializa todos los datos de parámetros etiquetados como en un búfer continuo para la transmisión al código auxiliar del servidor. Del mismo modo, el código auxiliar del servidor serializa todos los datos marcados con el atributo [**\[ out \]**](../midl/out-idl.md) en un búfer continuo para volver al código auxiliar del cliente. Aunque la capa de protocolo de red debajo de RPC puede fragmentar y crear paquetes en el búfer para la transmisión, la fragmentación es transparente para los códigos auxiliares de RPC.

La asignación de memoria para crear el marco de llamada del servidor puede ser una operación costosa. El código auxiliar del servidor intentará minimizar el uso innecesario de memoria cuando sea posible, y se supone que la rutina de servidor no liberará ni volverá a asociar los datos marcados con los atributos [**\[ de \]**](../midl/in.md) entrada o **\[ entrada. \]** El código auxiliar del servidor intenta reutilizar los datos en el búfer siempre que sea posible para evitar la duplicación innecesaria. La regla general es que si el formato de datos serializados es el mismo que el formato de memoria, RPC usará punteros a los datos serializados en lugar de asignar memoria adicional para datos con el mismo formato.

Por ejemplo, la siguiente llamada RPC se define con una estructura cuyo formato serializado es idéntico al formato en memoria.

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

En este caso, RPC no asigna memoria adicional para los datos a los que hace referencia *plInStructure*; en su lugar, simplemente pasa el puntero a los datos serializados a la implementación de la función del lado servidor. El código auxiliar del servidor RPC comprueba el búfer durante el proceso de desmarque si el código auxiliar se compila con la marca "-robust" (que es una configuración predeterminada en la versión más reciente del compilador MIDL). RPC garantiza que los datos pasados a la implementación de la función del lado servidor son válidos.

Tenga en cuenta que la memoria se asigna para *plOutStructure*, ya que no se pasa ningún dato al servidor para ella.

## <a name="memory-allocation-for-inbound-data"></a>Asignación de memoria para datos entrantes

Pueden surgir casos en los que el código auxiliar del servidor asigna memoria para los datos de parámetros marcados con [**\[ los atributos de \]**](../midl/in.md) entrada o **\[ entrada. \]** Esto ocurre cuando el formato de datos serializados difiere del formato de memoria, o cuando las estructuras que componen los datos serializados son suficientemente complejas y el código auxiliar del servidor RPC debe leerlo de forma atómica. A continuación se muestran varios casos comunes en los que se debe asignar memoria para los datos recibidos por el código auxiliar del servidor.

-   Los datos son una matriz variable o una matriz variable compatible. Se trata de matrices (o punteros a matrices) que tienen establecido el atributo [**\[ \_ length is() \]**](../midl/length-is.md) o first [**\[ \_ is(). \]**](../midl/first-is.md) En MULTIDIMENSIONAL, solo se serializa y transmite el primer elemento de estas matrices. Por ejemplo, en el fragmento de código siguiente, los datos pasados en el parámetro *pv* tendrán memoria asignada.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Los datos son una cadena de tamaño o una cadena no compatible. Estas cadenas suelen ser punteros a datos de caracteres etiquetados [**\[ con el atributo size \_ is(). \]**](../midl/size-is.md) En el ejemplo siguiente, la cadena que se pasa a la función del lado servidor **SizedString** tendrá memoria asignada, mientras que la cadena que se pasa a la función **NormalString** se reutilizará.

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   Los datos son un tipo simple cuyo tamaño de memoria difiere de su tamaño serializado, como **enum16** e **\_ \_ int3264.**
-   Los datos se definen mediante una estructura cuya alineación de memoria es menor que la alineación natural, contiene cualquiera de los tipos de datos anteriores o tiene relleno de bytes final. Por ejemplo, la siguiente estructura de datos compleja ha forzado la alineación de 2 bytes y tiene relleno al final.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Los datos contienen una estructura que se debe serializar campo por campo. Estos campos incluyen punteros de interfaz definidos en interfaces DCOM; punteros omitido; valores enteros establecidos con el atributo [**\[ range; \]**](../midl/range.md) elementos de matrices definidos con la serialización de [**\[ \_ \]**](../midl/transmit-as.md) [**\[ \_ \] conexión,**](../midl/wire-marshal.md) [**\[ \_ \]**](../midl/user-marshal.md)serialización de usuario, transmisión como y [**\[ representación \_ \]**](../midl/represent-as.md) como atributos; y estructuras de datos complejas incrustadas.
-   Los datos contienen una unión, una estructura que contiene una unión o una matriz de uniones. Solo la rama específica de la unión se serializa en la conexión.
-   Los datos contienen una estructura con una matriz compatible multidimensional que tiene al menos una dimensión no fija.
-   Los datos contienen una matriz de estructuras complejas.
-   Los datos contienen una matriz de tipos de datos simples, como **enum16** e **\_ \_ int3264.**
-   Los datos contienen una matriz de punteros ref e interface.
-   Los datos tienen un [**\[ atributo force \_ allocate \]**](../midl/force-allocate.md) aplicado a un puntero.
-   Los datos tienen un [**\[ atributo allocate(all \_ nodes) \]**](../midl/allocate.md) aplicado a un puntero.
-   Los datos tienen un [**\[ atributo de recuento \_ de \]**](../midl/byte-count.md) bytes aplicado a un puntero.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Sintaxis de transferencia de datos de 64 bits y TRANSFER64

Como se mencionó anteriormente, los datos de 64 bits se pueden obtener mediante una sintaxis de transferencia de 64 bits específica denominada QL64. Esta sintaxis de transferencia se desarrolló para solucionar el problema específico que surge cuando los punteros se serializan en QL de 32 bits y se transmiten a un código auxiliar de servidor en una plataforma de 64 bits. En este caso, un puntero de datos de 32 bits serializado no coincide con uno de 64 bits y la asignación de memoria se producirá invariablemente. Para crear un comportamiento más coherente en plataformas de 64 bits, Microsoft desarrolló una nueva sintaxis de transferencia denominada COHERENCIA64.

Un ejemplo que ilustra este problema es el siguiente:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Esta estructura, cuando se serializa, la reutilizará el código auxiliar del servidor en un sistema de 32 bits. Sin embargo, si el código auxiliar del servidor reside en un sistema de 64 bits, los datos serializados por LENGTH tienen una longitud de 4 bytes, pero el tamaño de memoria necesario será de 8. Como resultado, se fuerza la asignación de memoria y rara vez se producirá la reutilización del búfer. MOUSE64 soluciona este problema haciendo que el tamaño serializado de un puntero de 64 bits.

A diferencia de MULTIDIMENSIONAL de 32 bits, los tipos de datos simples, como **enum16** e **\_ \_ int3264,** no hacen que una estructura o matriz sea compleja en MULTIDIMENSIONAL64. Del mismo modo, los valores de panel finales no hacen que una estructura sea compleja. Los punteros de interfaz se tratan como punteros únicos en el nivel superior; como resultado, las estructuras y matrices que contienen punteros de interfaz no se consideran complejas y no requerirán una asignación de memoria específica para su uso.

## <a name="initializing-outbound-data"></a>Inicialización de datos salientes

Una vez que se han desmarcronado todos los datos de entrada, el código auxiliar del servidor debe inicializar los punteros de solo salida marcados con el [**\[ atributo out. \]**](../midl/out-idl.md)


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



En la llamada anterior, el código auxiliar del servidor debe inicializar *plOutStructure* porque no estaba presente en los datos serializados y es un puntero [**\[ ref \]**](../midl/ref.md) implícito que debe estar disponible para la implementación de la función de servidor. El código auxiliar del servidor RPC inicializa y cero cualquier puntero de nivel superior solo de referencia con el [**\[ atributo out. \]**](../midl/out-idl.md) Los **\[ punteros \]** de referencia de salida que hay debajo de él también se inicializan de forma recursiva. La recursividad se detiene en cualquier puntero con [**\[ los atributos \] únicos**](../midl/unique.md) o [**\[ ptr \]**](../midl/ptr.md) establecidos en ellos.

La implementación de la función de servidor no puede modificar directamente los valores de puntero de nivel superior y, por tanto, no puede volver asignárlos. Por ejemplo, en la implementación de **ProcessRpcStructure** anterior, el código siguiente no es válido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure es* un valor de pila y su cambio no se propaga de nuevo a RPC. La implementación de la función de servidor puede intentar evitar la asignación intentando liberar *plOutStructure,* lo que puede provocar daños en la memoria. A continuación, el código auxiliar del servidor asignará espacio para el puntero de nivel superior en memoria (en el caso de puntero a puntero) y una estructura simple de nivel superior cuyo tamaño en la pila es menor de lo esperado.

En determinadas circunstancias, el cliente puede especificar el tamaño de asignación de memoria del lado servidor. En el ejemplo siguiente, el cliente especifica el tamaño de los datos salientes en el parámetro de *tamaño de* entrada.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Después de desmarmar los datos entrantes, incluido el tamaño *,* el código auxiliar del servidor asigna un búfer para *pv* con un tamaño de "sizeof(char) \* size". Una vez asignado el espacio, el código auxiliar del servidor cero el búfer. Tenga en cuenta que, en este caso concreto, el código auxiliar asigna la memoria con el usuario **de MIDL \_ \_ allocate()**, ya que el tamaño del búfer se determina en tiempo de ejecución.

Tenga en cuenta que, en el caso de las interfaces DCOM, es posible que los códigos auxiliares generados por MIDL no participen en absoluto si el cliente y el servidor comparten el mismo apartamento COM o si se implementa **ICallFrame.** En este caso, el servidor no puede depender del comportamiento de asignación y debe comprobar de forma independiente la memoria de tamaño de cliente.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementaciones de funciones del lado servidor y serialización de datos salientes

Inmediatamente después de la desmarshalling en los datos entrantes y la inicialización de la memoria asignada para contener datos salientes, el código auxiliar del servidor RPC ejecuta la implementación del lado servidor de la función a la que llama el cliente. En este momento, el servidor puede modificar los datos marcados específicamente con el atributo **\[ in, out \]** y puede rellenar la memoria asignada para los datos de solo salida (los datos etiquetados con [**\[ out \]**](../midl/out-idl.md)).

Las reglas generales para la manipulación de datos de parámetros de referencia son sencillas: el servidor solo puede asignar nueva memoria o modificar la memoria asignada específicamente por el código auxiliar del servidor. La reasignación o liberación de memoria existente para los datos puede tener un impacto negativo en los resultados y el rendimiento de la llamada de función, y puede ser muy difícil de depurar.

Lógicamente, el servidor RPC reside en un espacio de direcciones diferente que el cliente y, por lo general, se puede suponer que no comparten memoria. Como resultado, es seguro que la implementación de la función de servidor use los datos marcados con el atributo [**\[ in \]**](../midl/in.md) como memoria "scratch" sin afectar a las direcciones de memoria del cliente. Dicho esto, el servidor no debe intentar **\[ \]** volver a asignación ni liberar datos, dejando el control de esos espacios en el propio código auxiliar del servidor RPC.

Por lo general, la implementación de la función de servidor no necesita volver a asignación ni liberar datos marcados con el **\[ atributo in y \]** out. En el caso de los datos de tamaño fijo, la lógica de implementación de la función puede modificar directamente los datos. Del mismo modo, para los datos de tamaño variable, la implementación de la función tampoco debe modificar el valor de campo proporcionado al [**\[ atributo size \_ \] is().**](../midl/size-is.md) Cambie el valor de campo utilizado para cambiar el tamaño de los resultados de los datos en un búfer más pequeño o mayor devuelto al cliente que puede estar mal equipado para tratar con la longitud anómala.

Si se producen circunstancias en las que la rutina de servidor tiene que volver a asignar la memoria usada por los datos marcados con el atributo **\[ in, out, \]** es totalmente posible que la implementación de la función del lado servidor no sepa si el puntero proporcionado por el código auxiliar es para la memoria asignada con el usuario **de MIDL \_ \_ allocate()** o el búfer de conexión serializado. Para solucionar este problema, MS RPC puede asegurarse de que no se produzca ninguna pérdida de memoria o daños si el atributo [**\[ force \_ allocate \]**](../midl/force-allocate.md) está establecido en los datos. Cuando **\[ se establece force \_ allocate, \]** el código auxiliar del servidor siempre asignará memoria para el puntero, aunque la advertencia es que el rendimiento disminuirá para cada uso de él.

Cuando la llamada vuelve de la implementación de la función del lado servidor, el código auxiliar del servidor serializa los datos marcados con el atributo [**\[ out \]**](../midl/out-idl.md) y los envía al cliente. Tenga en cuenta que el código auxiliar no serializa los datos si la implementación de la función del lado servidor produce una excepción.

## <a name="releasing-allocated-memory"></a>Liberar memoria asignada

El código auxiliar del servidor RPC liberará la memoria de pila después de que la llamada haya devuelto desde la función del lado servidor, independientemente de si se produce una excepción o no. El código auxiliar del servidor libera toda la memoria asignada por el código auxiliar, así como cualquier memoria asignada con **midl \_ user \_ allocate().** La implementación de la función del lado servidor siempre debe proporcionar a RPC un estado coherente, ya sea iniciando una excepción o devolviendo un código de error. Si se produce un error en la función durante la población de estructuras de datos complicadas, debe asegurarse de que todos los punteros apuntan a datos válidos o se establecen en **NULL.**

Durante este paso, el código auxiliar del servidor libera toda la memoria que no forma parte del búfer serializado que contiene en [**\[ los \]**](../midl/in.md) datos. Una excepción a este comportamiento son los datos con el atributo [**\[ allocate(don't \_ free) \]**](../midl/allocate.md) establecido en ellos: el código auxiliar del servidor no libera ninguna memoria asociada a estos punteros.

Después de que el código auxiliar del servidor libera la memoria asignada por el código auxiliar y la implementación de la función, el código auxiliar llama a una función de notificación específica si se especifica el atributo de marca [**\[ de \_ \]**](../midl/notify-flag.md) notificación para determinados datos.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshalling a Linked List over RPC : un ejemplo


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



En el ejemplo anterior, el formato de memoria para **LINKEDLIST** será idéntico al formato de conexión serializada. Como resultado, el código auxiliar del servidor no asigna memoria para toda la cadena de punteros de datos en *pIn*. En su lugar, RPC reutiliza el búfer de conexión para toda la lista vinculada. Del mismo modo, el código auxiliar no asigna memoria para *pInOut*, sino que reutiliza el búfer de conexión serializado por el cliente.

Dado que la firma de función contiene un parámetro de salida, *pOut*, el código auxiliar del servidor asigna memoria para contener los datos devueltos. La memoria asignada se establece inicialmente en ceros, con **pNext** establecido en **NULL.** La aplicación puede asignar la memoria para una nueva lista vinculada y apuntar *pOut* -> **pNext** a ella. *pIn* y la lista vinculada que contiene se pueden usar como un área cero, pero la aplicación no debe cambiar ninguno de los punteros pNext.

La aplicación puede cambiar libremente el contenido de la lista vinculada a la que apunta *pInOut*, pero no debe cambiar ninguno de los punteros **pNext,** y mucho menos el propio vínculo de nivel superior. Si la aplicación decide acortar la lista vinculada, no puede saber si un puntero **pNext** determinado vincula a un búfer interno rpc o a un búfer asignado específicamente con el usuario **\_ \_ allocate() de MIDL.** Para evitar este problema, agregue una declaración de tipo específica para los punteros de lista vinculada que fuerza la asignación de usuarios, como se muestra en el código siguiente.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Este atributo obliga al código auxiliar del servidor a asignar cada nodo de la lista vinculada por separado y la aplicación puede liberar la parte abreviada de la lista vinculada llamando a **usuario de MIDL \_ \_ free().** La aplicación puede establecer de forma segura el puntero **pNext** al final de la lista vinculada recién abreviada en **NULL.**

 

 