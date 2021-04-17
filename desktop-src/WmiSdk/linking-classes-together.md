---
description: Los proveedores de WMI normalmente están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Vincular clases juntas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697644"
---
# <a name="linking-classes-together"></a><span data-ttu-id="d6b05-103">Vincular clases juntas</span><span class="sxs-lookup"><span data-stu-id="d6b05-103">Linking Classes Together</span></span>

<span data-ttu-id="d6b05-104">Los proveedores de WMI normalmente están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo.</span><span class="sxs-lookup"><span data-stu-id="d6b05-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="d6b05-105">Si hay una propiedad común que puede actuar como una clave para identificar de forma exclusiva todas las instancias de origen diferentes, use el [proveedor de vistas](view-provider.md) para combinar propiedades de diferentes clases, espacios de nombres o equipos en una sola clase.</span><span class="sxs-lookup"><span data-stu-id="d6b05-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="d6b05-106">Primero debe [registrar el proveedor de vistas](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d6b05-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="d6b05-107">Después del registro, puede crear los siguientes tipos de clases de vista:</span><span class="sxs-lookup"><span data-stu-id="d6b05-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="d6b05-108">Vista de combinación</span><span class="sxs-lookup"><span data-stu-id="d6b05-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="d6b05-109">Instancias de clases diferentes conectadas por un valor de propiedad común.</span><span class="sxs-lookup"><span data-stu-id="d6b05-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="d6b05-110">Vista de asociación</span><span class="sxs-lookup"><span data-stu-id="d6b05-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="d6b05-111">Vistas de clases de asociación existentes en el límite del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d6b05-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="d6b05-112">Vista Unión</span><span class="sxs-lookup"><span data-stu-id="d6b05-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="d6b05-113">Unión de una o más instancias.</span><span class="sxs-lookup"><span data-stu-id="d6b05-113">Union of one or more instances.</span></span>

 

 



