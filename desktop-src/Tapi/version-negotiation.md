---
description: Con el tiempo, pueden existir diferentes versiones para las aplicaciones TAPI, TAPI y los proveedores de servicios.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negociación de las versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002748"
---
# <a name="version-negotiation"></a><span data-ttu-id="e455c-103">Negociación de las versiones</span><span class="sxs-lookup"><span data-stu-id="e455c-103">Version Negotiation</span></span>

<span data-ttu-id="e455c-104">Con el tiempo, pueden existir diferentes versiones para las aplicaciones TAPI, TAPI y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="e455c-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="e455c-105">La interoperabilidad óptima de una aplicación TAPI requiere conocimiento de no solo la versión de TAPI de la aplicación, sino también de la DLL de TAPI, TAPISVR y las versiones del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="e455c-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="e455c-106">Si no se realiza la negociación de la versión correcta, pueden producirse problemas graves.</span><span class="sxs-lookup"><span data-stu-id="e455c-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="e455c-107">Por ejemplo, algunas estructuras de uso intensivo tienen miembros de datos agregados de una versión a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="e455c-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="e455c-108">Si el tamaño de la estructura no coincide con lo que la aplicación o TAPI espera, las consecuencias van desde pérdidas de memoria hasta AVs intermitente.</span><span class="sxs-lookup"><span data-stu-id="e455c-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="e455c-109">Para obtener más información, consulte [control de versiones de TAPI](./tapi-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="e455c-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="e455c-110">**TAPI 2. x:** Las aplicaciones negocian con TAPI y TAPISVR durante [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="e455c-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="e455c-111">Las aplicaciones realizan la negociación de dispositivos con proveedores de servicios mediante una llamada a [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) para cada línea que pueda usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e455c-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="e455c-112">**TAPI 3. x:** No es necesario realizar la negociación de la versión; sin embargo, puede usar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para determinar si una interfaz está disponible en su versión.</span><span class="sxs-lookup"><span data-stu-id="e455c-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
