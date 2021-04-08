---
title: API del complemento WinRM
description: La interfaz de programación de aplicaciones (API) de complementos de WinRM proporciona funcionalidad que permite a los usuarios escribir complementos mediante la implementación de ciertas API para los URI de recursos y las operaciones compatibles.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994385"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="897ff-103">API del complemento WinRM</span><span class="sxs-lookup"><span data-stu-id="897ff-103">WinRM Plug-in API</span></span>

<span data-ttu-id="897ff-104">Administración remota de Windows complementos son bibliotecas nativas de vínculos dinámicos (dll) que se conectan y amplían la funcionalidad de WinRM.</span><span class="sxs-lookup"><span data-stu-id="897ff-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="897ff-105">La interfaz de programación de aplicaciones (API) de complementos de WinRM proporciona funcionalidad que permite a los usuarios escribir complementos mediante la implementación de ciertas API para los [*URI de recursos*](windows-remote-management-glossary.md) y las operaciones compatibles.</span><span class="sxs-lookup"><span data-stu-id="897ff-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="897ff-106">Una vez configurados los complementos para el servicio WinRM o Internet Information Services (IIS), se cargan en el host de WinRM o en el host de IIS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="897ff-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="897ff-107">Las solicitudes remotas se enrutan a estos puntos de entrada del complemento para llevar a cabo las operaciones.</span><span class="sxs-lookup"><span data-stu-id="897ff-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="897ff-108">La sección de referencia de la API del complemento WinRM contiene información detallada acerca de los siguientes elementos de la API:</span><span class="sxs-lookup"><span data-stu-id="897ff-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="897ff-109">Puntos de entrada del complemento de autorización</span><span class="sxs-lookup"><span data-stu-id="897ff-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="897ff-110">Métodos de complemento de autorización</span><span class="sxs-lookup"><span data-stu-id="897ff-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="897ff-111">Puntos de entrada del complemento de operaciones</span><span class="sxs-lookup"><span data-stu-id="897ff-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="897ff-112">Métodos del complemento de operaciones</span><span class="sxs-lookup"><span data-stu-id="897ff-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="897ff-113">Estructuras</span><span class="sxs-lookup"><span data-stu-id="897ff-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




