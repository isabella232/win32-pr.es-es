---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Administración y mantenimiento de imágenes de implementación (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717056"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="8e013-103">Administración y mantenimiento de imágenes de implementación (DISM)</span><span class="sxs-lookup"><span data-stu-id="8e013-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8e013-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="8e013-104">Affected Platforms</span></span>

<span data-ttu-id="8e013-105">**Clientes** de Windows Vista SP1 y versiones posteriores \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e013-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="8e013-106">**Servidores** : windows Server 2008 RTM y versiones posteriores \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e013-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="8e013-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e013-107">Description</span></span>

<span data-ttu-id="8e013-108">La herramienta Administración y mantenimiento de imágenes de implementación (DISM) reemplaza a las herramientas PkgMgr, PEImg y IntlConfg que se están retirando en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e013-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="8e013-109">DISM proporciona una única herramienta centralizada para realizar todas las funciones de estas tres herramientas de una manera más eficaz y estandarizada, eliminando el origen de muchas de las frustraciones que experimentan los usuarios actuales de estas herramientas.</span><span class="sxs-lookup"><span data-stu-id="8e013-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="8e013-110">DISM incluye una corrección de compatibilidad para Windows Vista SP1 y versiones posteriores, así como para Windows Server 2008 RTM y versiones posteriores, que redirige las llamadas de PkgMgr desde las aplicaciones heredadas que se ejecutan en Windows 7 a DISM.</span><span class="sxs-lookup"><span data-stu-id="8e013-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="8e013-111">Si la aplicación se ejecuta en uno de los sistemas operativos compatibles, la corrección de compatibilidad enruta la llamada a PkgMgr.</span><span class="sxs-lookup"><span data-stu-id="8e013-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="8e013-112">No existe ninguna corrección de compatibilidad para las aplicaciones heredadas que llaman a PEImg o IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="8e013-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="8e013-113">Uso</span><span class="sxs-lookup"><span data-stu-id="8e013-113">Usage</span></span>

<span data-ttu-id="8e013-114">DISM es transparente para los usuarios finales de cualquiera de las plataformas admitidas.</span><span class="sxs-lookup"><span data-stu-id="8e013-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="8e013-115">Sin embargo, si una aplicación llama a PEImg o IntlConfg desde Windows 7, se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8e013-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="8e013-116">Actualice los scripts que llaman a PkgMgr, PEImg o IntlConfg para llamar a DISM en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8e013-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="8e013-117">Es importante incluir la actualización de los scripts de PkgMgr en este esfuerzo, ya que la corrección de compatibilidad que proporciona compatibilidad con versiones anteriores de PkgMgr se quitará en versiones futuras de los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="8e013-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="8e013-118">Asegúrese de que las llamadas a DISM han reemplazado las llamadas a PkgMgr, PEImg y IntlConfg, y que la operación se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e013-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e013-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e013-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8e013-120">[Administración y mantenimiento de imágenes de implementación (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8e013-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
