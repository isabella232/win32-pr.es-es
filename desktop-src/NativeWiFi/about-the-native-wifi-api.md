---
description: La API WiFi nativa contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Acerca de la API nativa WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279004"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="3420f-103">Acerca de la API nativa WiFi</span><span class="sxs-lookup"><span data-stu-id="3420f-103">About the Native Wifi API</span></span>

<span data-ttu-id="3420f-104">La API WiFi nativa contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos.</span><span class="sxs-lookup"><span data-stu-id="3420f-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="3420f-105">La API se puede usar para las redes de infraestructura y ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3420f-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="3420f-106">La API ad hoc inalámbrica es una interfaz simplificada orientada a objetos para crear, administrar y usar redes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3420f-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="3420f-107">El modo ad hoc podría no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="3420f-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="3420f-108">A partir de Windows 8.1 y Windows Server 2012 R2, utilice en su lugar [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="3420f-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="3420f-109">La implementación de la API ad hoc usa la API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="3420f-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="3420f-110">Esto significa que las llamadas de la API ad hoc pueden desencadenar notificaciones WiFi nativas y viceversa.</span><span class="sxs-lookup"><span data-stu-id="3420f-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="3420f-111">No se recomienda mezclar llamadas nativas de la API WiFi y llamadas inalámbricas de la API ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3420f-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="3420f-112">Los desarrolladores deben elegir un enfoque de programación antes de diseñar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3420f-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="3420f-113">Si su aplicación usa o administra redes de infraestructura, debe usar la API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="3420f-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="3420f-114">Si su aplicación requiere la funcionalidad de administración de perfiles, debe usar la API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="3420f-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="3420f-115">De lo contrario, debe usar la API ad hoc inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="3420f-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3420f-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3420f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3420f-117">Acerca de WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="3420f-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="3420f-118">Compatibilidad con la API WiFi nativa en Windows XP</span><span class="sxs-lookup"><span data-stu-id="3420f-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="3420f-119">Permisos de la API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="3420f-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="3420f-120">Acerca de la API ad hoc inalámbrica</span><span class="sxs-lookup"><span data-stu-id="3420f-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="3420f-121">Descargar el SDK de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3420f-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



