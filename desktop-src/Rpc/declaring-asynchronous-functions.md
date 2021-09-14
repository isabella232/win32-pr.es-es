---
title: Declarar funciones asincrónicas
description: Para declarar una función RPC como asincrónica, declare primero la función como parte de una definición de interfaz en un archivo de lenguaje de definición de interfaz (IDL).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Llamada a procedimiento remoto RPC, tareas, declaración de funciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069159"
---
# <a name="declaring-asynchronous-functions"></a>Declarar funciones asincrónicas

Para declarar una función RPC como asincrónica, declare primero la función como parte de una definición de interfaz en un archivo de lenguaje de definición de interfaz (IDL). El uso de funciones RPC asincrónicas no requiere ninguna modificación especial en el archivo IDL. En el ejemplo siguiente se muestra un archivo IDL para una aplicación que usa una función asincrónica.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Para todas las funciones RPC asincrónicas que usa la aplicación, deberá modificar la declaración de las funciones asincrónicas en el archivo ACF de la aplicación. Aplique el [**\[ atributo asincrónico a \]**](../midl/async.md) cada nombre de función asincrónica, como se muestra en el ejemplo siguiente:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Al aplicar el atributo **\[ asincrónico \]** en el archivo ACF, el compilador MIDL genera automáticamente un parámetro de identificador asincrónico adicional en el código auxiliar.

 

 