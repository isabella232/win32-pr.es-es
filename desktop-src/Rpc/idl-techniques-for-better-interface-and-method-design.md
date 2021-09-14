---
title: Técnicas de IDL para mejorar la interfaz y el diseño de métodos
description: Considere la posibilidad de usar las siguientes técnicas específicas de IDL para mejorar la seguridad y el rendimiento al desarrollar interfaces RPC y métodos que controlan datos compatibles y variantes.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244676"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Técnicas de IDL para mejorar la interfaz y el diseño de métodos

Considere la posibilidad de usar las siguientes técnicas específicas de IDL para mejorar la seguridad y el rendimiento al desarrollar interfaces RPC y métodos que controlan datos compatibles y variantes. Los atributos a los que se hace referencia en este tema son los atributos IDL establecidos en parámetros de método que controlan datos compatibles (por ejemplo, el tamaño es y max es atributos) o datos variantes \[ **\_** \] \[ **\_** \] (por ejemplo, \[ **\_** \] \[  los atributos length es y \] string).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Usar el \[ atributo range con parámetros de datos \] compatibles

El atributo range indica al rpc en tiempo de ejecución que realice una validación de tamaño adicional durante el \[  \] proceso de desmarque de datos. En concreto, comprueba que el tamaño proporcionado de los datos pasados como parámetro asociado está dentro del intervalo especificado.

El \[ **atributo range** \] no afecta al formato de conexión.

Si el valor de la conexión está fuera del intervalo permitido, RPC producirá una excepción RPC X INVALID BOUND o \_ RPC X BAD STUB \_ \_ \_ \_ \_ \_ DATA. Esto proporciona un nivel adicional de validación de datos y puede ayudar a evitar errores de seguridad comunes, como saturaciones de búfer. Del mismo modo, el uso del intervalo puede mejorar el rendimiento de la aplicación, ya que los datos compatibles marcados con él tienen restricciones claramente definidas disponibles para su consideración por \[  \] parte del servicio RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Reglas de administración de memoria de código auxiliar del servidor RPC

Es importante comprender las reglas de administración de memoria de código auxiliar del servidor RPC al crear los archivos IDL para una aplicación habilitada para RPC. Las aplicaciones pueden mejorar el uso de recursos de servidor mediante el uso del intervalo junto con los datos compatibles como se indicó anteriormente, así como evitar deliberadamente la aplicación de atributos IDL de datos de longitud variable, como length, para los datos \[  \] \[ **\_** \] compatibles.

No se recomienda la aplicación de longitud a los campos de estructura de datos definidos en un \[ **\_** \] archivo IDL.

## <a name="best-practices-for-variable-length-data-parameters"></a>Procedimientos recomendados para parámetros de datos de longitud variable

Los siguientes son varios procedimientos recomendados que se deben tener en cuenta al definir los atributos IDL para estructuras de datos de tamaño variable, parámetros de método y campos.

-   Use la correlación temprana. Por lo general, es mejor definir el parámetro o campo de tamaño variable, de modo que se produzca inmediatamente después del tipo entero de control.

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

    donde **earlyCorr declara el** parámetro de tamaño inmediatamente antes del parámetro de datos de longitud variable y **lateCorr** declara el parámetro size después de él. El uso de la correspondencia temprana mejora el rendimiento general, especialmente en los casos en los que se llama al método con frecuencia.

-   En el caso de los parámetros marcados con \[ **out, size \_** es la tupla de atributos y donde se conoce la longitud de datos en el lado cliente o donde el cliente tiene un límite superior razonable, la definición del método debe ser similar a la siguiente en términos de atribución y secuencia de \] parámetros:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    En este caso, el cliente proporciona un búfer de tamaño fijo para *pArr,* lo que permite al servicio RPC del lado servidor asignar un búfer de tamaño razonable con un buen grado de garantía. Tenga en cuenta que, en el ejemplo, los datos se reciben del servidor ( \[ **out** \] ). La definición es similar para los datos pasados al servidor ( \[ **en** \] ).

-   En situaciones en las que el componente del lado servidor de una aplicación RPC decide la longitud de los datos, la definición del método debe ser similar a la siguiente:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **RANGED \_ LONG** es un tipo definido para los códigos auxiliares de cliente y servidor, y de un tamaño especificado que el cliente puede prever correctamente. En el ejemplo, el cliente pasa *ppArr* como **NULL** y el componente de aplicación de servidor RPC asigna la cantidad correcta de memoria. Tras la devolución, el servicio RPC del lado cliente asigna la memoria para los datos devueltos.

-   Si el cliente desea enviar un subconjunto de una matriz compatible grande al servidor, la aplicación puede especificar el tamaño del subconjunto como se muestra en el ejemplo siguiente:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    De este modo, RPC solo transmitirá *elementos lLength* de la matriz a través de la conexión. Sin embargo, esta definición obliga al servicio RPC a asignar memoria de tamaño *lSize* en el lado servidor.

-   Si el componente de aplicación cliente determina el tamaño máximo de una matriz que el servidor puede devolver, pero permite que el servidor transmita un subconjunto de esa matriz, la aplicación puede especificar este comportamiento definiendo el IDL similar al ejemplo siguiente:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    El componente de aplicación cliente especifica el tamaño máximo de la matriz y el servidor especifica cuántos elementos transmite al cliente.

-   Si el componente de aplicación de servidor necesita devolver una cadena al componente de aplicación cliente y el cliente sabe el tamaño máximo que se va a devolver desde el servidor, la aplicación puede usar un tipo de cadena compatible como se muestra en el ejemplo siguiente:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Si el componente de aplicación cliente no debe controlar el tamaño de la cadena, el servicio RPC puede asignar específicamente la memoria como se muestra en el ejemplo siguiente:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    El componente de aplicación cliente debe establecer *ppStr* en **NULL** en al llamar al método RPC.

 

 




