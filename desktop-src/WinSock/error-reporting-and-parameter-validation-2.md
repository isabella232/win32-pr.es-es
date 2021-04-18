---
description: El esquema de informes de errores difiere entre las interfaces SPI y API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Informes de errores y validación de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705630"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="8f31c-103">Informes de errores y validación de parámetros</span><span class="sxs-lookup"><span data-stu-id="8f31c-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="8f31c-104">El esquema de informes de errores difiere entre las interfaces SPI y API.</span><span class="sxs-lookup"><span data-stu-id="8f31c-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="8f31c-105">Los proveedores de servicios de Windows Sockets notifican errores junto con la función que devuelve, en lugar del enfoque basado en subprocesos utilizado en la API.</span><span class="sxs-lookup"><span data-stu-id="8f31c-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="8f31c-106">El \_32.dll Ws2 utiliza el código de error por función del proveedor de servicios para actualizar el valor de error por subproceso que se obtiene a través de la función de la API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="8f31c-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="8f31c-107">Los proveedores de servicios siguen siendo necesarios, sin embargo, para mantener el error basado en sockets, que se puede recuperar mediante la \_ opción de socket de error.</span><span class="sxs-lookup"><span data-stu-id="8f31c-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="8f31c-108">El \_32.dll Ws2 realiza la validación de parámetros solo en las llamadas de función que se implementan completamente dentro de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="8f31c-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="8f31c-109">Los proveedores de servicios son responsables de realizar su propia validación de parámetros.</span><span class="sxs-lookup"><span data-stu-id="8f31c-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



