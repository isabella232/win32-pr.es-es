---
description: 'La API de gráficos usa las siguientes devoluciones de llamada:'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Devoluciones de llamada de la API de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082656"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="c9d41-103">Devoluciones de llamada de la API de gráficos</span><span class="sxs-lookup"><span data-stu-id="c9d41-103">Graphing API Callbacks</span></span>

<span data-ttu-id="c9d41-104">La API de gráficos usa las siguientes devoluciones de llamada:</span><span class="sxs-lookup"><span data-stu-id="c9d41-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="c9d41-105">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="c9d41-105">Callback</span></span>                                                          | <span data-ttu-id="c9d41-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9d41-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9d41-107">*PFNPEER \_ \_ datos de seguridad gratuitos \_*</span><span class="sxs-lookup"><span data-stu-id="c9d41-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="c9d41-108">Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para liberar los datos devueltos por el [*\_ \_ registro seguro de PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) y PFNPEER validar las devoluciones de llamada de [*\_ \_ registro*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) .</span><span class="sxs-lookup"><span data-stu-id="c9d41-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="c9d41-109">*\_registro seguro de PFNPEER \_*</span><span class="sxs-lookup"><span data-stu-id="c9d41-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="c9d41-110">Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para proteger los registros.</span><span class="sxs-lookup"><span data-stu-id="c9d41-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="c9d41-111">*PFNPEER \_ validar \_ registro*</span><span class="sxs-lookup"><span data-stu-id="c9d41-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="c9d41-112">Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para validar registros.</span><span class="sxs-lookup"><span data-stu-id="c9d41-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



