---
title: Configuración de la sesión de servidor
description: Configuración de la sesión de servidor
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090943"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="41ceb-103">Configuración de la sesión de servidor</span><span class="sxs-lookup"><span data-stu-id="41ceb-103">Configuring the Server Session</span></span>

<span data-ttu-id="41ceb-104">El identificador de sesión del servidor se crea con la [**función HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) y se usa en la llamada a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="41ceb-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="41ceb-105">El *parámetro pPropertyInformation* apunta a la estructura de configuración del tipo de propiedad que se establece.</span><span class="sxs-lookup"><span data-stu-id="41ceb-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="41ceb-106">El *parámetro PropertyInformationLength* especifica el tamaño, en bytes, de la estructura de configuración.</span><span class="sxs-lookup"><span data-stu-id="41ceb-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="41ceb-107">Por ejemplo, al establecer **HttpServerTimeoutsProperty,** el parámetro **pPropertyInformation** debe apuntar a un búfer que sea al menos el tamaño de la estructura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)</span><span class="sxs-lookup"><span data-stu-id="41ceb-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="41ceb-108">Normalmente, una aplicación HTTP crea una sesión de servidor único y puede establecer propiedades para toda la aplicación, como el límite de ancho de banda global o habilitar el registro centralizado en esta sesión de servidor.</span><span class="sxs-lookup"><span data-stu-id="41ceb-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="41ceb-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) invalida las configuraciones de LA API del servidor HTTP para la aplicación que realiza la llamada; no afecta a las propiedades de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="41ceb-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="41ceb-110">Las configuraciones de sesión del servidor se consultan mediante una llamada [**a HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="41ceb-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




