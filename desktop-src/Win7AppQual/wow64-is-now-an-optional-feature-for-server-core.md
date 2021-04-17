---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Estado de WoW64 en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707290"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="133c1-103">WoW64 es ahora una característica opcional de Server Core</span><span class="sxs-lookup"><span data-stu-id="133c1-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="133c1-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="133c1-104">Affected Platforms</span></span>

<span data-ttu-id="133c1-105">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="133c1-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="133c1-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="133c1-106">Feature Impact</span></span>

 <span data-ttu-id="133c1-107">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="133c1-107">**Severity** - Low</span></span>  
<span data-ttu-id="133c1-108">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="133c1-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="133c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="133c1-109">Description</span></span>

<span data-ttu-id="133c1-110">La opción de instalación Server Core para Windows Server 2008 R2 le permite desinstalar WoW64.</span><span class="sxs-lookup"><span data-stu-id="133c1-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="133c1-111">WoW64 es ahora una característica opcional que se puede desinstalar si no es necesario ejecutar código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="133c1-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="133c1-112">Además, los roles Active Directory y Active Directory Lightweight Directory Services requieren WoW64 para ejecutarse en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="133c1-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="133c1-113">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="133c1-113">Manifestation of Impact</span></span>

<span data-ttu-id="133c1-114">Si desinstala WoW64, los administradores que ejecuten código de 32 bits en Server Core recibirán un mensaje de error que indica que la aplicación no se puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="133c1-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="133c1-115">Si los administradores intentan ejecutar Active Directory y Active Directory Lightweight Directory Services, recibirán un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="133c1-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="133c1-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="133c1-116">Mitigation</span></span>

<span data-ttu-id="133c1-117">Instale WoW64.</span><span class="sxs-lookup"><span data-stu-id="133c1-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="133c1-118">Solución</span><span class="sxs-lookup"><span data-stu-id="133c1-118">Solution</span></span>

<span data-ttu-id="133c1-119">La solución preferida es proporcionar una versión de 64 bits del código para permitir que se ejecute en Server Core sin necesidad de WoW64.</span><span class="sxs-lookup"><span data-stu-id="133c1-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="133c1-120">Como mínimo, proporcione la documentación del usuario que indica que para ejecutar el código de 32 bits, deben instalar WoW64.</span><span class="sxs-lookup"><span data-stu-id="133c1-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="133c1-121">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="133c1-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="133c1-122">Compruebe que todo el código usado sea de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="133c1-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="133c1-123">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="133c1-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="133c1-124">Detalles de la implementación de WOW64</span><span class="sxs-lookup"><span data-stu-id="133c1-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="133c1-125">Depurar WOW64</span><span class="sxs-lookup"><span data-stu-id="133c1-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="133c1-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="133c1-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
