---
title: Acerca de la API del servidor HTTP
description: La API del servidor HTTP proporciona a los desarrolladores una interfaz de bajo nivel para el lado servidor de la funcionalidad HTTP, tal como se define en RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API de servidor HTTP, información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420344"
---
# <a name="about-http-server-api"></a><span data-ttu-id="16187-104">Acerca de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="16187-104">About HTTP Server API</span></span>

<span data-ttu-id="16187-105">La API del servidor HTTP proporciona a los desarrolladores una interfaz de bajo nivel para el lado servidor de la funcionalidad HTTP, tal como se define en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="16187-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="16187-106">La API permite a una aplicación recibir solicitudes HTTP dirigidas a direcciones URL y enviar respuestas HTTP.</span><span class="sxs-lookup"><span data-stu-id="16187-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="16187-107">Para enviar respuestas dinámicas, se recomiendan las interfaces ISAPI o ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="16187-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="16187-108">La API del servidor HTTP permite que varias aplicaciones coexistan en un sistema, compartiendo el mismo puerto TCP (por ejemplo, el puerto 80 para HTTP o el puerto 443 para HTTPS) y atendiendo a diferentes partes del espacio de nombres de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="16187-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="16187-109">La API del servidor HTTP requiere conocer el lenguaje de programación C y estar familiarizado con la programación de la API de Windows.</span><span class="sxs-lookup"><span data-stu-id="16187-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="16187-110">Las aplicaciones que no requieren acceso de bajo nivel a HTTP deben usar la ISAPI de IIS o las clases de .NET Framework para las soluciones basadas en HTTP.</span><span class="sxs-lookup"><span data-stu-id="16187-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




