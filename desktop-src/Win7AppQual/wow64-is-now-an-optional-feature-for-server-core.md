---
description: WoW64 es ahora una característica opcional para Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Estado de WoW64 en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084053"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="1fce4-103">WoW64 es ahora una característica opcional para Server Core</span><span class="sxs-lookup"><span data-stu-id="1fce4-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="1fce4-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="1fce4-104">Affected Platforms</span></span>

<span data-ttu-id="1fce4-105">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fce4-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="1fce4-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="1fce4-106">Feature Impact</span></span>

 <span data-ttu-id="1fce4-107">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="1fce4-107">**Severity** - Low</span></span>  
<span data-ttu-id="1fce4-108">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="1fce4-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="1fce4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fce4-109">Description</span></span>

<span data-ttu-id="1fce4-110">La opción de instalación Server Core para Windows Server 2008 R2 permite desinstalar WoW64.</span><span class="sxs-lookup"><span data-stu-id="1fce4-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="1fce4-111">WoW64 es ahora una característica opcional que se puede desinstalar si no es necesario ejecutar código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1fce4-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="1fce4-112">Además, los roles Active Directory y Active Directory Lightweight Directory Services requieren WoW64 para ejecutarse en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1fce4-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="1fce4-113">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="1fce4-113">Manifestation of Impact</span></span>

<span data-ttu-id="1fce4-114">Si desinstala WoW64, los administradores que ejecutan código de 32 bits en Server Core recibirán un mensaje de error que indica que no se puede ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1fce4-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="1fce4-115">Si los administradores intentan ejecutar Active Directory y Active Directory Lightweight Directory Services, recibirán un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1fce4-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="1fce4-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="1fce4-116">Mitigation</span></span>

<span data-ttu-id="1fce4-117">Instale WoW64.</span><span class="sxs-lookup"><span data-stu-id="1fce4-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="1fce4-118">Solución</span><span class="sxs-lookup"><span data-stu-id="1fce4-118">Solution</span></span>

<span data-ttu-id="1fce4-119">La solución preferida es proporcionar una versión de 64 bits del código para que se pueda ejecutar en Server Core sin necesidad de WoW64.</span><span class="sxs-lookup"><span data-stu-id="1fce4-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="1fce4-120">Como mínimo, proporcione documentación del usuario que note que para ejecutar código de 32 bits debe instalar WoW64.</span><span class="sxs-lookup"><span data-stu-id="1fce4-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="1fce4-121">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="1fce4-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="1fce4-122">Compruebe que todo el código usado es de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1fce4-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1fce4-123">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="1fce4-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="1fce4-124">Detalles de implementación de WOW64</span><span class="sxs-lookup"><span data-stu-id="1fce4-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="1fce4-125">Depuración de WOW64</span><span class="sxs-lookup"><span data-stu-id="1fce4-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="1fce4-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fce4-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
