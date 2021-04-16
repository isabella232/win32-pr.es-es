---
title: Tipos de datos de la API del servidor HTTP versión 1,0
description: La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el archivo de encabezado HTTP. h como enteros de 64 bits sin signo.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID tipo HTTP
- HTTP_RAW_CONNECTION_ID tipo HTTP
- HTTP_REQUEST_ID tipo HTTP
- HTTP_URL_CONTEXT tipo HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685616"
---
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="25096-107">Tipos de datos de la API del servidor HTTP versión 1,0</span><span class="sxs-lookup"><span data-stu-id="25096-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="25096-108">La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el archivo de encabezado HTTP. h como enteros de 64 bits sin signo (**ULONGLONGs**):</span><span class="sxs-lookup"><span data-stu-id="25096-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="25096-109">\_identificador de conexión HTTP \_</span><span class="sxs-lookup"><span data-stu-id="25096-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="25096-110">\_identificador de conexión http sin formato \_ \_</span><span class="sxs-lookup"><span data-stu-id="25096-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="25096-111">\_identificador de solicitud HTTP \_</span><span class="sxs-lookup"><span data-stu-id="25096-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="25096-112">\_contexto de URL http \_</span><span class="sxs-lookup"><span data-stu-id="25096-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="25096-113">Una aplicación no debe intentar generar o modificar ningún identificador que pertenezca a uno de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="25096-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




