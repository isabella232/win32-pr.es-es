---
title: Administración de memoria de código auxiliar de servidor
description: Administración de memoria de código auxiliar de servidor
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Administración de memoria de código auxiliar de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904871"
---
# <a name="server-stub-memory-management"></a>Administración de memoria de código auxiliar de servidor

## <a name="an-introduction-to-server-stub-memory-management"></a>Introducción a la administración de memoria de Server-Stub

Los códigos auxiliares generados por MIDL actúan como la interfaz entre un proceso de cliente y un proceso de servidor. Un código auxiliar de cliente calcula las referencias de todos los datos pasados a los parámetros marcados con el atributo [**\[ in \]**](../midl/in.md) y los envía al código auxiliar del servidor. El código auxiliar del servidor, al recibir estos datos, reconstruye la pila de llamadas y, a continuación, ejecuta la función de servidor implementada por el usuario correspondiente. El código auxiliar del servidor también calcula las referencias de los datos de parámetro marcados con el atributo [**\[ out \]**](../midl/out-idl.md) y lo devuelve a la aplicación cliente.

El formato de datos de serialización de bits de 32 usado por MSRPC es una versión compatible de la sintaxis de transferencia de representación de datos de red (NDR). Para obtener más información acerca de este formato, vea [el sitio web de Open Group](https://www.opengroup.org/). En el caso de las plataformas de 64 bits, se puede usar una extensión de Microsoft 64-bit a la sintaxis de transferencia de NDR denominada NDR64 para mejorar el rendimiento.

## <a name="unmarshaling-inbound-data"></a>Desserialización de datos de entrada

En MSRPC, el código auxiliar del cliente calcula las referencias de todos los datos de parámetro etiquetados como [**\[ en \]**](../midl/in.md) en un búfer continuo para la transmisión al código auxiliar del servidor. Del mismo modo, el código auxiliar del servidor calcula las referencias de todos los datos marcados con el atributo [**\[ out \]**](../midl/out-idl.md) en un búfer continuo para volver al código auxiliar del cliente. Mientras que la capa del Protocolo de red bajo RPC puede fragmentar y paquetes el búfer para la transmisión, la fragmentación es transparente para el código auxiliar de RPC.

La asignación de memoria para crear el marco de llamada del servidor puede ser una operación costosa. El código auxiliar del servidor intentará minimizar el uso de memoria innecesario cuando sea posible y se supone que la rutina del servidor no liberará ni reasignará los datos marcados con los atributos de **\[ salida \]** [**\[ in \]**](../midl/in.md) o in. El código auxiliar del servidor intenta reutilizar los datos en el búfer siempre que sea posible para evitar la duplicación innecesaria. La regla general es que si el formato de los datos de cálculo de referencias es el mismo que el formato de memoria, RPC usará punteros a los datos de cálculo de referencias en lugar de asignar memoria adicional para datos con el mismo formato.

Por ejemplo, la siguiente llamada RPC se define con una estructura cuyo formato de serialización es idéntico al formato en memoria.

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

En este caso, RPC no asigna memoria adicional para los datos a los que hace referencia *plInStructure*; en su lugar, simplemente pasa el puntero a los datos de cálculo de referencias a la implementación de la función del servidor. El código auxiliar del servidor RPC comprueba el búfer durante el proceso de desserialización si el código auxiliar se compila con la marca "-robusta" (que es un valor predeterminado en la versión nmost reciente del compilador de MIDL). RPC garantiza que los datos que se pasan a la implementación de la función del servidor son válidos.

Tenga en cuenta que la memoria se asigna para *plOutStructure*, ya que no se pasa ningún dato al servidor para ella.

## <a name="memory-allocation-for-inbound-data"></a>Asignación de memoria para los datos de entrada

Pueden surgir casos en los que el código auxiliar del servidor asigna memoria a los datos de parámetros marcados con los atributos [**\[ in \]**](../midl/in.md) o **\[ in, out \]** . Esto se produce cuando el formato de datos con cálculo de referencias difiere del formato de memoria o cuando las estructuras que componen los datos serializados son suficientemente complejas y el código auxiliar del servidor RPC debe leerlos de forma atómica. A continuación se enumeran varios casos comunes en los que se debe asignar memoria para los datos recibidos por el código auxiliar del servidor.

-   Los datos son una matriz variable o una matriz variable compatible. Son matrices (o punteros a matrices) que tienen la [**\[ longitud \_ () \]**](../midl/length-is.md) o el [**\[ primer atributo \_ is () \]**](../midl/first-is.md) establecido en ellos. En NDR, solo se calculan las referencias de los primeros elementos de estas matrices y se transmiten. Por ejemplo, en el fragmento de código siguiente, los datos pasados en el parámetro *PV* tendrán la memoria asignada.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Los datos son una cadena de tamaño o una cadena no compatible. Estas cadenas suelen ser punteros a datos de caracteres etiquetados con el atributo [**\[ size \_ es () \]**](../midl/size-is.md) . En el ejemplo siguiente, la cadena que se pasa a la función del lado servidor **SizedString** tendrá asignada la memoria, mientras que la cadena que se pasa a la función **NormalString** se volverá a usar.

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

-   Los datos son un tipo simple cuyo tamaño de memoria difiere del tamaño de las referencias calculadas, como **enum16** y **\_ \_ int3264**.
-   Los datos se definen mediante una estructura cuya alineación de memoria es menor que la alineación natural, contiene cualquiera de los tipos de datos anteriores o tiene un relleno de bytes final. Por ejemplo, la estructura de datos compleja siguiente tiene una alineación forzada de 2 bytes y tiene relleno al final.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Los datos contienen una estructura en la que se deben calcular las referencias de campo por campo. Estos campos incluyen punteros de interfaz definidos en interfaces DCOM; punteros omitidos; valores enteros establecidos con el atributo [**\[ de \] intervalo**](../midl/range.md) ; elementos de matrices definidas con las [**\[ \_ \] referencias de conexión**](../midl/wire-marshal.md), [**\[ \_ serialización \] de usuario**](../midl/user-marshal.md), [**\[ transmitir \_ como \]**](../midl/transmit-as.md) y [**\[ representan \_ como \]**](../midl/represent-as.md) atributos; y estructuras de datos complejos incrustados.
-   Los datos contienen una Unión, una estructura que contiene una Unión o una matriz de uniones. Solo se calculan las referencias de la rama específica de la Unión en la conexión.
-   Los datos contienen una estructura con una matriz compatible multidimensional que tiene al menos una dimensión no fija.
-   Los datos contienen una matriz de estructuras complejas.
-   Los datos contienen una matriz de tipos de datos simples, como **enum16** y **\_ \_ int3264**.
-   Los datos contienen una matriz de punteros Ref y de interfaz.
-   Los datos tienen un atributo [**\[ Force \_ allocate \]**](../midl/force-allocate.md) aplicado a un puntero.
-   Los datos tienen un atributo [**\[ allocate (todos los \_ nodos) \]**](../midl/allocate.md) aplicado a un puntero.
-   Los datos tienen un atributo de [**\[ \_ recuento \] de bytes**](../midl/byte-count.md) aplicado a un puntero.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>Sintaxis de transferencia de datos y NDR64 de 64 bits

Como se mencionó anteriormente, se calculan las referencias de los datos de 64 bits usando una sintaxis de transferencia de 64 bits específica denominada NDR64. Esta sintaxis de transferencia se desarrolló para abordar el problema específico que se produce cuando se serializan los punteros en un NDR de 32 bits y se transmiten a un código auxiliar de servidor en una plataforma de 64 bits. En este caso, un puntero de datos de 32 bits serializado no coincide con una de 64 bits y la asignación de memoria se realizará invariablemente. Para crear un comportamiento más coherente en las plataformas de 64 bits, Microsoft desarrolló una nueva sintaxis de transferencia denominada NDR64.

A continuación se muestra un ejemplo que ilustra este problema:


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Esta estructura, cuando se calculan las referencias, la reutilizará el código auxiliar del servidor en un sistema de 32 bits. Sin embargo, si el código auxiliar del servidor reside en un sistema de 64 bits, los datos de serialización de NDR tienen una longitud de 4 bytes, pero el tamaño de memoria necesario será 8. Como resultado, se fuerza la asignación de memoria y la reutilización del búfer rara vez se producirá. NDR64 soluciona este problema, ya que hace que el tamaño de las referencias de un puntero sea de 64 bits.

A diferencia del NDR de 32 bits, tyes de datos simples, como **enum16** y **\_ \_ int3264** , no convierten una estructura o una matriz compleja en NDR64. Del mismo modo, los valores de relleno finales no hacen que una estructura sea compleja. Los punteros de interfaz se tratan como punteros únicos en el nivel superior; como resultado, las estructuras y matrices que contienen punteros de interfaz no se consideran complejas y no requieren una asignación de memoria específica para su uso.

## <a name="initializing-outbound-data"></a>Inicializar datos salientes

Una vez que se han desordenado todos los datos de entrada, el código auxiliar del servidor debe inicializar los punteros solo salientes marcados con el atributo [**\[ out \]**](../midl/out-idl.md) .


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



En la llamada anterior, el código auxiliar del servidor debe inicializar *plOutStructure* porque no estaba presente en los datos de cálculo de referencias y es un puntero de [**\[ referencia \]**](../midl/ref.md) implícito que debe estar disponible para la implementación de la función de servidor. El código auxiliar del servidor RPC inicializa y pone en cero los punteros de solo referencia de nivel superior con el atributo [**\[ out \]**](../midl/out-idl.md) . Los punteros de referencia que se encuentran debajo de él también se inicializan de forma recursiva. **\[ \]** La recursividad se detiene en cualquier puntero con los atributos [**\[ Unique \]**](../midl/unique.md) o [**\[ ptr \]**](../midl/ptr.md) establecidos.

La implementación de la función de servidor no puede modificar directamente los valores de puntero de nivel superior y, por tanto, no puede reasignarlos. Por ejemplo, en la implementación de **ProcessRpcStructure** anterior, el código siguiente no es válido:


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* es un valor de pila y su cambio no se propaga de nuevo a RPC. La implementación de la función de servidor puede intentar evitar la asignación al intentar liberar *plOutStructure*, lo que puede provocar daños en la memoria. El código auxiliar del servidor asignará espacio para el puntero de nivel superior en memoria (en el caso de puntero a puntero) y una estructura simple de nivel superior cuyo tamaño en la pila sea menor de lo esperado.

En determinadas circunstancias, el cliente puede especificar el tamaño de asignación de memoria del lado del servidor. En el ejemplo siguiente, el cliente especifica el tamaño de los datos salientes en el parámetro de *tamaño* de entrada.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Después de desreferenciar los datos de entrada, incluido el *tamaño*, el código auxiliar del servidor asigna un búfer para *PV* con un tamaño de "sizeof (Char) \* size". Una vez asignado el espacio, el código auxiliar del servidor pone en cero el búfer. Tenga en cuenta que, en este caso concreto, el código auxiliar asigna la memoria con el **usuario de MIDL \_ \_ allocate ()**, ya que el tamaño del búfer se determina en tiempo de ejecución.

Tenga en cuenta que en el caso de las interfaces DCOM, es posible que los códigos auxiliares generados por MIDL no participen en absoluto si el cliente y el servidor comparten el mismo apartamento COM, o si se implementa **ICallFrame** . En este caso, el servidor no puede depender del comportamiento de asignación y debe comprobar de forma independiente la memoria de tamaño del cliente.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implementaciones de funciones de servidor y serialización de datos de salida

Inmediatamente después de la desserialización en los datos de entrada y la inicialización de la memoria asignada que contiene los datos de salida, el código auxiliar del servidor RPC ejecuta la implementación del lado servidor de la función a la que llama el cliente. En este momento, el servidor puede modificar los datos marcados específicamente con el atributo **\[ in \] , out** y puede rellenar la memoria asignada para los datos de solo salida (los datos etiquetados con [**\[ out \]**](../midl/out-idl.md)).

Las reglas generales para la manipulación de datos de parámetros de cálculo de referencias son simples: el servidor solo puede asignar una nueva memoria o modificar la memoria asignada específicamente por el código auxiliar del servidor. La reasignación o liberación de la memoria existente para los datos puede tener un impacto negativo en los resultados y en el rendimiento de la llamada de función, y puede ser muy difícil de depurar.

Lógicamente, el servidor RPC reside en un espacio de direcciones diferente del cliente y, por lo general, se puede suponer que no comparten memoria. Como resultado, es seguro que la implementación de la función de servidor use los datos marcados con el atributo [**\[ in \]**](../midl/in.md) como memoria "temporal" sin afectar a las direcciones de memoria del cliente. Dicho esto, el servidor no debería intentar volver a asignar **\[ \] o liberar datos** , y dejar el control de esos espacios al propio código auxiliar del servidor RPC.

Por lo general, la implementación de la función de servidor no necesita reasignar o liberar los datos marcados con el atributo **\[ in, out \]** . En el caso de los datos de tamaño fijo, la lógica de implementación de la función puede modificar los datos directamente. Del mismo modo, para los datos de tamaño variable, la implementación de la función no debe modificar el valor del campo proporcionado al atributo [**\[ size \_ es () \]**](../midl/size-is.md) , ya sea. Cambiar el valor del campo usado para cambiar el tamaño de los resultados de los datos en un búfer más pequeño o más grande devuelto al cliente, que puede estar mal equipado para tratar la longitud anómala.

Si se producen circunstancias en las que la rutina del servidor tiene que reasignar la memoria utilizada por los datos marcados con el atributo **\[ in, out \]** , es posible que la implementación de la función de servidor no sepa si el puntero proporcionado por el código auxiliar es a la memoria asignada con el usuario de la asignación de los **usuarios de MIDL \_ \_ ()** o el búfer de conexión de serialización. Para solucionar este problema, MS RPC puede garantizar que no se produzcan pérdidas de memoria o daños si se establece el atributo [**\[ Force \_ allocate \]**](../midl/force-allocate.md) en los datos. Cuando se establece **\[ Force \_ allocate \]** , el código auxiliar del servidor asignará siempre la memoria para el puntero, aunque la advertencia es que el rendimiento se reducirá para cada uso de la misma.

Cuando se devuelve la llamada desde la implementación de función del servidor, el código auxiliar del servidor calcula las referencias de los datos marcados con el atributo [**\[ out \]**](../midl/out-idl.md) y los envía al cliente. Tenga en cuenta que el código auxiliar no calcula las referencias de los datos si la implementación de la función del servidor produce una excepción.

## <a name="releasing-allocated-memory"></a>Liberar memoria asignada

El código auxiliar del servidor RPC liberará la memoria de la pila una vez que se haya devuelto la llamada desde la función del servidor, tanto si se produce una excepción como si no. El código auxiliar de servidor libera toda la memoria asignada por el código auxiliar y cualquier memoria asignada con la **asignación de usuarios de MIDL \_ \_ ()**. La implementación de la función de servidor siempre debe proporcionar a RPC un estado coherente, ya sea iniciando una excepción o devolviendo un código de error. Si se produce un error en la función durante el rellenado de estructuras de datos complicadas, debe asegurarse de que todos los punteros señalan a datos válidos o que están establecidos en **null**.

Durante este paso, el código auxiliar del servidor libera toda la memoria que no forma parte del búfer de serialización que contiene los datos [**\[ de \]**](../midl/in.md) . Una excepción a este comportamiento son los datos con el atributo [**\[ allocate (no \_ Free) \]**](../midl/allocate.md) establecido en ellos: el código auxiliar del servidor no libera ninguna memoria asociada a estos punteros.

Una vez que el código auxiliar del servidor libera la memoria asignada por el código auxiliar y la implementación de la función, el código auxiliar llama a una función de notificación específica si se especifica el atributo de [**\[ \_ marca \]**](../midl/notify-flag.md) de notificación para datos determinados.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Serialización de una lista vinculada a través de RPC: ejemplo


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



En el ejemplo anterior, el formato de memoria de **LINKEDLIST** será idéntico al formato de conexión con cálculo de referencias. Como resultado, el código auxiliar del servidor no asigna memoria para toda la cadena de punteros de datos en el *código pIn*. En su lugar, RPC reutiliza el búfer de conexión para toda la lista vinculada. Del mismo modo, el código auxiliar no asigna memoria para el *pines*, sino que vuelve a usar el búfer de conexión serializado por el cliente.

Dado que la firma de la función contiene un parámetro de salida, *pOut*, el código auxiliar del servidor asigna memoria para que contenga los datos devueltos. La memoria asignada es inicialmente cero, con **pNext** establecido en **null**. La aplicación puede asignar la memoria para una nueva lista vinculada y apuntar *pOut* -> **pNext** a ella. el *pIn* y la lista vinculada que contiene se pueden usar como un área temporal, pero la aplicación no debe cambiar ninguno de los punteros pNext.

La aplicación puede cambiar libremente el contenido de la lista vinculada a la que apunta el *pines*, pero no debe cambiar ninguno de los punteros **pNext** , por lo que solo se permite el vínculo de nivel superior. Si la aplicación decide acortar la lista vinculada, no puede saber si alguno de los vínculos de puntero **pNext** especificados para un búfer interno de RPC o un búfer asignado específicamente con **MIDL \_ User \_ allocate ()**. Para evitar este problema, se agrega una declaración de tipos específica para los punteros de lista vinculados que fuerza la asignación del usuario, tal como se muestra en el código siguiente.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Este atributo obliga al código auxiliar del servidor a asignar cada nodo de la lista vinculada por separado, y la aplicación puede liberar la parte abreviada de la lista vinculada llamando a **MIDL \_ \_ Free ()**. A continuación, la aplicación puede establecer de forma segura el puntero **pNext** al final de la lista vinculada recién acortada en **null**.

 

 