---
description: Administración y mantenimiento de imágenes de implementación (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Administración y mantenimiento de imágenes de implementación (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088493"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="33e50-103">Administración y mantenimiento de imágenes de implementación (DISM)</span><span class="sxs-lookup"><span data-stu-id="33e50-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="33e50-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="33e50-104">Affected Platforms</span></span>

<span data-ttu-id="33e50-105">**Clientes:** Windows Vista SP1 y \| versiones posteriores de Windows 7</span><span class="sxs-lookup"><span data-stu-id="33e50-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="33e50-106">**Servidores:** Windows Server 2008 RTM y \| versiones posteriores de Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33e50-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="33e50-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="33e50-107">Description</span></span>

<span data-ttu-id="33e50-108">La herramienta Administración y mantenimiento de imágenes de implementación (DISM) reemplaza las herramientas pkgmgr, PEImg e IntlConfg que se van a retirar en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33e50-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="33e50-109">DISM proporciona una única herramienta centralizada para realizar todas las funciones de estas tres herramientas de una manera más eficaz y estandarizada, lo que elimina el origen de muchas de las frustraciones que experimentan los usuarios actuales de estas herramientas.</span><span class="sxs-lookup"><span data-stu-id="33e50-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="33e50-110">DISM incluye una corrección de compatibilidad (shim) para Windows Vista SP1 y versiones posteriores, así como para Windows Server 2008 RTM y versiones posteriores, que redirige las llamadas de pkgmgr desde aplicaciones heredadas que se ejecutan en Windows 7 a DISM.</span><span class="sxs-lookup"><span data-stu-id="33e50-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="33e50-111">Si la aplicación se ejecuta en uno de los sistemas operativos compatibles, la corrección de compatibilidad (shim) enruta la llamada a pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="33e50-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="33e50-112">No existen correcciones de compatibilidad (shim) para las aplicaciones heredadas que llaman a PEImg o IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="33e50-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="33e50-113">Uso</span><span class="sxs-lookup"><span data-stu-id="33e50-113">Usage</span></span>

<span data-ttu-id="33e50-114">DISM es transparente para los usuarios finales de pkgmgr en cualquiera de las plataformas admitidas.</span><span class="sxs-lookup"><span data-stu-id="33e50-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="33e50-115">Sin embargo, si una aplicación llama a PEImg o IntlConfg desde Windows 7, se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="33e50-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="33e50-116">Actualice los scripts que llaman a pkgmgr, PEImg o IntlConfg para llamar a DISM en su lugar.</span><span class="sxs-lookup"><span data-stu-id="33e50-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="33e50-117">Es importante incluir la actualización de scripts de pkgmgr en este esfuerzo, ya que la corrección de compatibilidad con versiones anteriores de pkgmgr se quitará en versiones futuras de los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="33e50-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="33e50-118">Asegúrese de que las llamadas a DISM han reemplazado las llamadas a pkgmgr, PEImg e IntlConfg, y que la operación se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="33e50-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33e50-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33e50-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="33e50-120">[Administración y mantenimiento de imágenes de implementación (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="33e50-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
