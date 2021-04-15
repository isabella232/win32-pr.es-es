---
title: Disponibilidad de los controladores de gráficos aplicables en Windows Update
description: La disponibilidad de estos controladores en Windows Update (WU) determinará si a un usuario se le ofrece automáticamente una actualización de Windows 7, Windows 8 o Windows 8.1 a Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695292"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="48c17-103">Disponibilidad de los controladores de gráficos aplicables en Windows Update</span><span class="sxs-lookup"><span data-stu-id="48c17-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="48c17-104">La disponibilidad de estos controladores en Windows Update (WU) determinará si a un usuario se le ofrece automáticamente una actualización de Windows 7, Windows 8 o Windows 8.1 a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="48c17-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="48c17-105">Si los análisis de hardware mostraron que no había ningún controlador de gráficos disponible en Windows Update para el adaptador de gráficos del equipo, no se ofrecía al usuario el sistema operativo Windows 10 actualizado.</span><span class="sxs-lookup"><span data-stu-id="48c17-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="48c17-106">Sin embargo, los usuarios todavía pueden obtener Windows 10 a través de otros orígenes y realizar la actualización manualmente.</span><span class="sxs-lookup"><span data-stu-id="48c17-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="48c17-107">Algunos usuarios no estaban seguros de por qué no se les ofrecía la actualización cuando otras personas, aunque el asesor de actualizaciones explicó que no había ningún controlador de gráficos disponible para su hardware.</span><span class="sxs-lookup"><span data-stu-id="48c17-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="48c17-108">Además, algunos usuarios forzaban una actualización y, a continuación, detectaban que la funcionalidad de gráficos y el rendimiento sufrieron debido a la falta de un controlador de hardware.</span><span class="sxs-lookup"><span data-stu-id="48c17-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="48c17-109">Mitigaciones</span><span class="sxs-lookup"><span data-stu-id="48c17-109">Mitigations</span></span>

<span data-ttu-id="48c17-110">Para mitigar esto, los usuarios pueden instalar manualmente un controlador anterior, es decir, desde Windows 7, Windows 8 o Windows 8.1, yendo al sitio web de IHV o OEM y descargando un controlador explícitamente.</span><span class="sxs-lookup"><span data-stu-id="48c17-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="48c17-111">Esto debe hacerse después de la actualización y no se garantiza que funcione.</span><span class="sxs-lookup"><span data-stu-id="48c17-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="48c17-112">No hay ninguna solución compatible Si un controlador de gráficos adecuado no está disponible en WU.</span><span class="sxs-lookup"><span data-stu-id="48c17-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="48c17-113">El usuario debe decidir si:</span><span class="sxs-lookup"><span data-stu-id="48c17-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="48c17-114">Permanecer en el sistema operativo anterior;</span><span class="sxs-lookup"><span data-stu-id="48c17-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="48c17-115">Acepte las limitaciones del controlador de software, el adaptador de pantalla básico de Microsoft (MSBDA). de</span><span class="sxs-lookup"><span data-stu-id="48c17-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="48c17-116">Compre una nueva tarjeta gráfica que tenga un controlador compatible con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="48c17-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="48c17-117">Soluciones</span><span class="sxs-lookup"><span data-stu-id="48c17-117">Solutions</span></span>

<span data-ttu-id="48c17-118">Es fundamental que los fabricantes de equipos originales (IHV) carguen sus controladores de gráficos de Windows 10 en WU para cualquier hardware que pretendan admitir.</span><span class="sxs-lookup"><span data-stu-id="48c17-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="48c17-119">Tenga en cuenta que el hardware que ha alcanzado el final de la vida (EOL) podría no tener controladores en WU.</span><span class="sxs-lookup"><span data-stu-id="48c17-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="48c17-120">En este caso, no hay ninguna solución: el usuario debe elegir una de las opciones de mitigaciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="48c17-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




