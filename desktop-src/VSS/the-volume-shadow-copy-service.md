---
description: El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en sistemas basados en Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: El Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809853"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="34c91-103">El Servicio de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="34c91-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="34c91-104">El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en sistemas basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="34c91-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="34c91-105">Aunque es muy transparente para el usuario y el desarrollador, VSS hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="34c91-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="34c91-106">Coordina las actividades de proveedores, escritores y solicitantes en la creación y el uso de instantáneas</span><span class="sxs-lookup"><span data-stu-id="34c91-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="34c91-107">Facilita el proveedor del sistema predeterminado</span><span class="sxs-lookup"><span data-stu-id="34c91-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="34c91-108">Implementa la funcionalidad de controlador de bajo nivel necesaria para que cualquier proveedor funcione</span><span class="sxs-lookup"><span data-stu-id="34c91-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="34c91-109">El servicio VSS se inicia a petición, de modo que, para que las operaciones de VSS se realicen correctamente, este servicio debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="34c91-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



