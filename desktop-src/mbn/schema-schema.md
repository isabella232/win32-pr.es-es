---
description: Define un perfil de banda ancha móvil.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Referencia de esquema de Perfil de banda ancha móvil
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666504"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="a437b-103">Referencia de esquema de Perfil de banda ancha móvil</span><span class="sxs-lookup"><span data-stu-id="a437b-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="a437b-104">El esquema de Perfil de banda ancha móvil define un perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="a437b-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="a437b-105">Los perfiles almacenan los parámetros de configuración de red y de usuario relacionados con la conexión de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="a437b-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="a437b-106">También almacenan las preferencias de usuario para una conexión.</span><span class="sxs-lookup"><span data-stu-id="a437b-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="a437b-107">El elemento raíz de un perfil de banda ancha móvil es el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a437b-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="a437b-108">Cada perfil tiene exactamente un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="a437b-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="a437b-109">Todos los elementos de esquema de Perfil de banda ancha móvil usados por Windows 7 se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v1` y los elementos usados por Windows 8 se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="a437b-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="a437b-110">El esquema de Perfil de banda ancha móvil exige estrictamente el orden de los nodos.</span><span class="sxs-lookup"><span data-stu-id="a437b-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="a437b-111">Los nodos especificados en un perfil deben adherirse al **esquema de Perfil de banda ancha móvil** y aparecer en el orden indicado en la definición del esquema.</span><span class="sxs-lookup"><span data-stu-id="a437b-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="a437b-112">Por ejemplo, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) debe especificarse inmediatamente después de [**AccessString**](schema-accessstring-contexttype-element.md).</span><span class="sxs-lookup"><span data-stu-id="a437b-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="a437b-113">Esquema de Perfil de banda ancha móvil v1</span><span class="sxs-lookup"><span data-stu-id="a437b-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="a437b-114">Esquema de Perfil de banda ancha móvil V2</span><span class="sxs-lookup"><span data-stu-id="a437b-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="a437b-115">Esquema de Perfil de banda ancha móvil V3</span><span class="sxs-lookup"><span data-stu-id="a437b-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="a437b-116">[Esquema de Perfil de banda ancha móvil V4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a437b-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
