---
title: Declarar funciones asincrónicas
description: Para declarar una función RPC como asincrónica, primero declare la función como parte de una definición de interfaz en un archivo de lenguaje de definición de interfaz (IDL).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Llamada a procedimiento remoto RPC, tareas, declarar funciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995703"
---
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="b4314-104">Declarar funciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="b4314-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="b4314-105">Para declarar una función RPC como asincrónica, primero declare la función como parte de una definición de interfaz en un archivo de lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="b4314-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="b4314-106">El uso de funciones RPC asincrónicas no requiere ninguna modificación especial en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b4314-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="b4314-107">En el ejemplo siguiente se muestra un archivo IDL para una aplicación que utiliza una función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b4314-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

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

<span data-ttu-id="b4314-108">Para todas las funciones RPC asincrónicas que usa la aplicación, debe modificar la declaración de las funciones asincrónicas en el archivo ACF de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4314-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="b4314-109">Aplique el atributo [**\[ Async \]**](../midl/async.md) a cada nombre de función asincrónica, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b4314-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="b4314-110">Al aplicar el atributo **\[ Async \]** en el archivo ACF, el compilador MIDL genera automáticamente un parámetro de identificador asincrónico adicional en el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b4314-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 