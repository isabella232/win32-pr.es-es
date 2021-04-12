---
title: Características de la API del servidor HTTP
description: En este tema se admiten las características admitidas y no admitidas de la API del servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Características de la API del servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357582"
---
# <a name="http-server-api-features"></a><span data-ttu-id="c4882-104">Características de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="c4882-104">HTTP Server API Features</span></span>

<span data-ttu-id="c4882-105">En las listas siguientes se describen las características admitidas y no admitidas de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4882-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="c4882-106">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="c4882-106">Features Supported</span></span>

<span data-ttu-id="c4882-107">HTTP admite las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="c4882-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="c4882-108">Funcionalidad de servidor de HTTP v 1.0 y v 1.1.</span><span class="sxs-lookup"><span data-stu-id="c4882-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="c4882-109">Capa de sockets seguros 3,0 (SSL) compatible con los certificados de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="c4882-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="c4882-110">Almacenamiento en caché de fragmentos de datos para su uso en respuestas posteriores.</span><span class="sxs-lookup"><span data-stu-id="c4882-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="c4882-111">Compatibilidad con direcciones IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="c4882-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="c4882-112">Reservas de espacio de nombres URL para la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4882-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="c4882-113">Controladores verdaderos para todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="c4882-113">True handles for all objects.</span></span>
-   <span data-ttu-id="c4882-114">Modelos de e/s sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="c4882-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="c4882-115">Compatibilidad con WOW64 en equipos que ejecutan Windows de 64 bits a partir de Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c4882-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="c4882-116">Características no admitidas</span><span class="sxs-lookup"><span data-stu-id="c4882-116">Features Not Supported</span></span>

<span data-ttu-id="c4882-117">La API del servidor HTTP no admite la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4882-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="c4882-118">La API del servidor HTTP no realiza la autenticación del cliente o del servidor basándose en el contenido de los encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4882-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="c4882-119">La aplicación debe implementar cualquier autenticación necesaria.</span><span class="sxs-lookup"><span data-stu-id="c4882-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="c4882-120">WOW64 en equipos que ejecutan Windows de 64 bits no se admite en Windows Server 2003 y Windows XP con Service Pack 2 (SP2) y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c4882-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="c4882-121">La API del servidor HTTP no admite el registro de solicitudes y respuestas HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4882-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="c4882-122">La API del servidor HTTP no fragmenta las respuestas HTTP salientes.</span><span class="sxs-lookup"><span data-stu-id="c4882-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="c4882-123">La aplicación debe implementar la fragmentación de la respuesta si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c4882-123">The application must implement response chunking if required.</span></span>

 

 




