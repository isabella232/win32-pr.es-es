---
title: Mejoras del analizador
description: Mejoras del analizador
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Mejoras del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418885"
---
# <a name="parser-enhancements"></a><span data-ttu-id="45619-104">Mejoras del analizador</span><span class="sxs-lookup"><span data-stu-id="45619-104">Parser Enhancements</span></span>

<span data-ttu-id="45619-105">En Windows Server 2003 con Service Pack 1 (SP1), la API del servidor HTTP permite las siguientes solicitudes de clientes HTTP.</span><span class="sxs-lookup"><span data-stu-id="45619-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="45619-106">Solicitudes que utilizan una fuente de una sola línea (LF) como terminadores de línea.</span><span class="sxs-lookup"><span data-stu-id="45619-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="45619-107">Las solicitudes que contienen espacios en blanco lineales (LWS) entre la línea de solicitud HTTP y el inicio de los encabezados.</span><span class="sxs-lookup"><span data-stu-id="45619-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="45619-108">Estos comportamientos están habilitados de forma predeterminada y no se controlan mediante la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="45619-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




