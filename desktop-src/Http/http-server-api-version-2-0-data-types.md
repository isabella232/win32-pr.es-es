---
title: Tipos de datos de la API del servidor HTTP versión 2,0
description: Tipos de datos de la API del servidor HTTP versión 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665707"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="07dee-103">Tipos de datos de la API del servidor HTTP versión 2,0</span><span class="sxs-lookup"><span data-stu-id="07dee-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="07dee-104">La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el encabezado HTTP. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="07dee-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="07dee-105">**USHORT** \_ \_ \_ \_ parámetro de tiempo de espera de configuración de servicio http, \* PHTTP de tiempo de espera de \_ configuración de servicio \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="07dee-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="07dee-106">**ULONGLONG** \_identificador opaco \_ de http \* , \_ \_ ID. de PHTTP opaco</span><span class="sxs-lookup"><span data-stu-id="07dee-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="07dee-107">**Http \_ identificador \_** de solicitud HTTP de ID. opaco \_ \_ , \* \_ \_ ID. de solicitud de PHTTP</span><span class="sxs-lookup"><span data-stu-id="07dee-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="07dee-108">**Http \_ identificador \_** \_ de conexión HTTP \_ de identificador opaco, \* \_ ID. de conexión de PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="07dee-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="07dee-109">**Http \_ identificador \_ opaco** identificador \_ de conexión http sin formato, ID. \_ \_ de \* \_ conexión sin formato de PHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="07dee-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="07dee-110">**USHORT** \_ \_ \_ \_ parámetro de tiempo de espera de configuración de servicio http, \* PHTTP de tiempo de espera de \_ configuración de servicio \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="07dee-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="07dee-111">Una aplicación no debe intentar generar o modificar ningún identificador que pertenezca a uno de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="07dee-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




