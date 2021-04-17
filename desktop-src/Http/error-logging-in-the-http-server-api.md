---
title: Error Logging in the HTTP Server API
description: La API del servidor HTTP controla algunos tipos de errores en lugar de devolverlos a una aplicación para controlarlos, ya que la frecuencia de estos errores podría inundar un registro de eventos o un controlador de aplicación.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API del servidor HTTP, registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685484"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="5317f-104">Error Logging in the HTTP Server API</span><span class="sxs-lookup"><span data-stu-id="5317f-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="5317f-105">La API del servidor HTTP controla algunos tipos de errores en lugar de devolverlos a una aplicación para controlarlos, ya que la frecuencia de estos errores podría inundar un registro de eventos o un controlador de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5317f-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="5317f-106">En los siguientes tres temas se describen los distintos aspectos del registro de errores de la API del servidor HTTP:</span><span class="sxs-lookup"><span data-stu-id="5317f-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="5317f-107">[Configuración](configuring-http-server-api-error-logging.md) de Los valores del registro controlan si la API del servidor HTTP registra errores, el tamaño máximo permitido de los archivos de registro y dónde se guardan los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="5317f-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="5317f-108">[Formato del archivo de registro](format-of-the-http-server-api-error-logs.md) La API del servidor HTTP crea archivos de registro que cumplen las convenciones del archivo de registro del World Wide Web Consortium (W3C) y se pueden analizar mediante herramientas estándar.</span><span class="sxs-lookup"><span data-stu-id="5317f-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="5317f-109">Sin embargo, a diferencia de los archivos de registro del W3C, los archivos de registro de la API del servidor HTTP no contienen los nombres de las columnas.</span><span class="sxs-lookup"><span data-stu-id="5317f-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="5317f-110">[Tipos de errores registrados](types-of-errors-logged-by-the-http-server-api.md) La API del servidor HTTP registra diversos errores comunes.</span><span class="sxs-lookup"><span data-stu-id="5317f-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




