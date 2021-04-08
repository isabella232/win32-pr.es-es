---
title: MSAA no está disponible para las aplicaciones de la tienda Windows
description: MSAA no está disponible para las aplicaciones de la tienda Windows
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078505"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="5e2ba-103">MSAA no está disponible para las aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="5e2ba-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="5e2ba-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="5e2ba-104">Platform</span></span>

<span data-ttu-id="5e2ba-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="5e2ba-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="5e2ba-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e2ba-106">Description</span></span>

<span data-ttu-id="5e2ba-107">Windows 8 no es compatible con MSAA (Microsoft Active Accessibility) para leer o automatizar datos accesibles desde aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="5e2ba-108">En su lugar, se debe usar la API de automatización de la interfaz de usuario (UIA), disponible desde Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="5e2ba-109">Dado que no hay ninguna característica existente de la aplicación de la tienda Windows, no hay implementaciones existentes que se vean afectadas por este cambio.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="5e2ba-110">Esto afecta solo a las nuevas aplicaciones y características escritas para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="5e2ba-111">Los desarrolladores pueden seguir usando MSAA para exponer sus datos de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="5e2ba-112">Si el proveedor de aplicaciones de la tienda Windows proporciona los datos de MSAA, los clientes de UIA todavía podrán leer y automatizar los datos.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="5e2ba-113">Para simplificar la API de las aplicaciones de la tienda Windows 8Windows, decidimos admitir solo la automatización de la interfaz de usuario como cliente para estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="5e2ba-114">Los clientes de UIA pueden leer proveedores de UIA de forma nativa, sin traducción.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="5e2ba-115">Los clientes de UIA pueden leer proveedores de MSAA como traducidos a través del proxy de UIA a MSAA.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="5e2ba-116">Esto reducirá la carga de pruebas de los desarrolladores de aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="5e2ba-117">La eliminación de la compatibilidad con los proveedores de MSAA reduciría aún más la matriz de pruebas, pero hay aplicaciones importantes que siguen estando basadas en MSAA y no queremos representarlas inaccesibles.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5e2ba-118">Manifestación</span><span class="sxs-lookup"><span data-stu-id="5e2ba-118">Manifestation</span></span>

<span data-ttu-id="5e2ba-119">Los desarrolladores de aplicaciones de la tienda Windows no podrán acceder a los detalles de MSAA en el modelo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="5e2ba-120">Solución</span><span class="sxs-lookup"><span data-stu-id="5e2ba-120">Solution</span></span>

<span data-ttu-id="5e2ba-121">No se deben crear nuevos casos automatizados en MSAA para las características de las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="5e2ba-122">Cambie las herramientas integradas existentes que usan MSAA a UIA si necesitan interactuar con las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="5e2ba-123">Los desarrolladores de aplicaciones de la tienda Windows deben usar la API de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e2ba-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="5e2ba-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="5e2ba-124">Resources</span></span>

-   [<span data-ttu-id="5e2ba-125">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="5e2ba-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 