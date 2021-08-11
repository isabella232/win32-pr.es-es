---
title: Técnicas de IDL para mejorar el diseño de la interfaz y el método
description: Considere la posibilidad de utilizar las siguientes técnicas específicas de IDL para mejorar la seguridad y el rendimiento cuando desarrolle interfaces y métodos RPC que controlen los datos de variantes y compatibles.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418621"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Técnicas de IDL para mejorar el diseño de la interfaz y el método

Considere la posibilidad de utilizar las siguientes técnicas específicas de IDL para mejorar la seguridad y el rendimiento cuando desarrolle interfaces y métodos RPC que controlen los datos de variantes y compatibles. Los atributos a los que se hace referencia en este tema son los atributos IDL establecidos en los parámetros de método que controlan los datos compatibles (por ejemplo, los \[ atributos **size \_ is** \] y \[ **Max \_ is** \] ) o Variant (por ejemplo, la \[ **longitud \_ es** \] y los atributos de \[ **cadena** \] ).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Usar el \[ \] atributo Range con parámetros de datos compatibles

El \[  \] atributo Range indica al tiempo de ejecución de RPC que realice la validación de tamaño adicional durante el proceso de desserialización de datos. En concreto, comprueba que el tamaño proporcionado de los datos pasados como parámetro asociado está dentro del intervalo especificado.

El \[ atributo de **intervalo** no \] afecta al formato de conexión.

Si el valor de la conexión está fuera del intervalo permitido, RPC producirá una \_ excepción de \_ datos de \_ \_ \_ \_ código auxiliar \_ de RPC x no válido o no válido de RPC x. Esto proporciona un nivel adicional de validación de datos y puede ayudar a evitar errores de seguridad comunes, como saturaciones del búfer. Del mismo modo, el uso de \[ **Range** \] puede mejorar el rendimiento de las aplicaciones, ya que los datos conformes marcados con él tienen restricciones claramente definidas que pueden tener en cuenta el servicio RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Reglas de administración de memoria de código auxiliar de servidor RPC

Es importante comprender las reglas de administración de memoria de código auxiliar de servidor RPC al crear los archivos IDL para una aplicación habilitada para RPC. Las aplicaciones pueden mejorar la utilización de recursos del servidor mediante el uso \[  \] de intervalos junto con los datos conformes indicados anteriormente, así como la prevención deliberada de atributos IDL de longitud variable, como la \[ **longitud, \_ es** \] para los datos compatibles.

No se recomienda la aplicación de \[ **longitud \_** \] a los campos de la estructura de datos definidos en un archivo IDL.

## <a name="best-practices-for-variable-length-data-parameters"></a>Prácticas recomendadas para los parámetros de datos de longitud variable

A continuación se muestran varios procedimientos recomendados que se deben tener en cuenta al definir los atributos IDL para estructuras de datos de tamaño variable, parámetros de método y campos.

-   Usar la correlación temprana. Por lo general, es mejor definir el parámetro o el campo de tamaño variable de forma que se produzca inmediatamente después del tipo entero de control.

    Por ejemplo,

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    es mejor que

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    donde **earlyCorr** declara el parámetro de tamaño inmediatamente antes del parámetro de datos de longitud variable y **lateCorr** declara el parámetro de tamaño después. El uso de la correspondencia temprana mejora el rendimiento en general, especialmente en los casos en los que se llama al método con frecuencia.

-   En el caso de los parámetros marcados con \[ **out, size \_ es** \] una tupla de atributo y donde la longitud de los datos se conoce en el lado del cliente o el cliente tiene un límite superior razonable, la definición del método debe ser similar a la siguiente en cuanto a la atribución de parámetros y a la secuencia:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    En este caso, el cliente proporciona un búfer de tamaño fijo para *pArr*, lo que permite que el servicio RPC del servidor asigne un búfer de tamaño razonable con un buen grado de seguridad. Tenga en cuenta que, en el ejemplo, los datos se reciben del servidor ( \[ **out** \] ). La definición es similar para los datos pasados al servidor ( \[ **en** \] ).

-   En situaciones en las que el componente del lado servidor de una aplicación RPC decide la longitud de los datos, la definición del método debe ser similar a la siguiente:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **Con \_ intervalo LONG** es un tipo definido para el código auxiliar de cliente y de servidor, y de un tamaño especificado que el cliente puede prever correctamente. En el ejemplo, el cliente pasa *ppArr* como **null** y el componente de aplicación de servidor RPC asigna la cantidad de memoria correcta. En el momento de la devolución, el servicio RPC en el lado cliente asigna la memoria para los datos devueltos.

-   Si el cliente desea enviar un subconjunto de una matriz grande compatible al servidor, la aplicación puede especificar el tamaño del subconjunto tal como se muestra en el ejemplo siguiente:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    De este modo, RPC solo transmitirá elementos *lLength* de la matriz a través de la conexión. Sin embargo, esta definición obliga al servicio RPC a asignar memoria de tamaño *Lsize* en el lado del servidor.

-   Si el componente de aplicación cliente determina el tamaño máximo de una matriz que el servidor puede devolver, pero permite que el servidor transmita un subconjunto de esa matriz, la aplicación puede especificar este tipo de comportamiento definiendo el IDL de forma similar al ejemplo siguiente:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    El componente de aplicación cliente especifica el tamaño máximo de la matriz y el servidor especifica el número de elementos que devuelve al cliente.

-   Si el componente de aplicación de servidor necesita devolver una cadena al componente de aplicación cliente y si el cliente conoce el tamaño máximo que se va a devolver del servidor, la aplicación puede usar un tipo de cadena compatible como se muestra en el ejemplo siguiente:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Si el componente de aplicación cliente no debe controlar el tamaño de la cadena, el servicio RPC puede asignar específicamente la memoria tal como se muestra en el ejemplo siguiente:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    El componente de aplicación cliente debe establecer *ppStr* en **null** cuando se llama al método RPC.

 

 




