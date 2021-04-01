---
description: Más información acerca de los errores del motor de almacenamiento extensible
title: Errores del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913585"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="c09aa-103">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="c09aa-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="c09aa-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c09aa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="c09aa-105">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="c09aa-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="c09aa-106">Todos los errores posibles devueltos por la API del motor de almacenamiento extensible (ESE) se definen mediante el tipo de datos [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="c09aa-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="c09aa-107">Para obtener una lista de las marcas de error definidas para esta API, vea [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c09aa-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="c09aa-108">En la documentación de la API de ESE, solo se documentan los errores más importantes.</span><span class="sxs-lookup"><span data-stu-id="c09aa-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="c09aa-109">Estos errores suelen representar errores de uso de la API o condiciones de error muy importantes.</span><span class="sxs-lookup"><span data-stu-id="c09aa-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="c09aa-110">Tenga en cuenta que cualquiera de estas API de ESE también puede devolver otros errores que no están documentados para cada API.</span><span class="sxs-lookup"><span data-stu-id="c09aa-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="c09aa-111">En estos casos, el autor de la llamada simplemente debe controlar el error como cualquier otro error devuelto por la API.</span><span class="sxs-lookup"><span data-stu-id="c09aa-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="c09aa-112">El valor de error específico se puede usar para fines de diagnóstico como el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c09aa-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="c09aa-113">En general, un valor mayor que cero debe interpretarse como una advertencia, el valor cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error.</span><span class="sxs-lookup"><span data-stu-id="c09aa-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="c09aa-114">No es necesario que una aplicación confíe en otros patrones de estos valores (por ejemplo, intervalos de valores).</span><span class="sxs-lookup"><span data-stu-id="c09aa-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="c09aa-115">Cuando ESE encuentra algunos de los errores más graves, crea una entrada en el registro de eventos que contiene detalles sobre los errores.</span><span class="sxs-lookup"><span data-stu-id="c09aa-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="c09aa-116">El nivel de registro se puede controlar mediante [parámetros del registro de eventos](./event-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c09aa-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="c09aa-117">Algunas aplicaciones requieren la capacidad de devolver [JET_ERR](./jet-err.md)s como valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c09aa-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="c09aa-118">En el siguiente ejemplo de C++ se muestra cómo hacer esa conversión:</span><span class="sxs-lookup"><span data-stu-id="c09aa-118">The following C++ example shows how to make that conversion:</span></span>

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

<span data-ttu-id="c09aa-119">Para obtener información sobre cómo configurar los parámetros del sistema para el control de errores, consulte [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c09aa-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="c09aa-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c09aa-120">See Also</span></span>

[<span data-ttu-id="c09aa-121">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="c09aa-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="c09aa-122">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="c09aa-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="c09aa-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c09aa-123">JET_ERR</span></span>](./jet-err.md)
