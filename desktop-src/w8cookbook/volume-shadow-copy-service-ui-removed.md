---
title: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
description: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488406"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="fc330-103">Interfaz de usuario de versiones anteriores quitada para volúmenes locales</span><span class="sxs-lookup"><span data-stu-id="fc330-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="fc330-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="fc330-104">Platform</span></span>

<span data-ttu-id="fc330-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="fc330-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="fc330-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc330-106">Description</span></span>

<span data-ttu-id="fc330-107">Las versiones anteriores de Windows permitían a los usuarios restaurar versiones anteriores de archivos individuales desde "instantáneas" de volúmenes locales.</span><span class="sxs-lookup"><span data-stu-id="fc330-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="fc330-108">Estas instantáneas se crean mediante la característica "versiones anteriores" a través del servicio de instantáneas de volumen (VSS).</span><span class="sxs-lookup"><span data-stu-id="fc330-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="fc330-109">En Windows 7, los usuarios pueden configurar y programar instantáneas en la interfaz de usuario de protección del sistema disponible a través de las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc330-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="fc330-110">Sin embargo, las versiones anteriores se usaban con poca frecuencia y afectaban negativamente al rendimiento general de Windows; como resultado, se ha quitado la característica.</span><span class="sxs-lookup"><span data-stu-id="fc330-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="fc330-111">En Windows 8, estas características ya no están disponibles:</span><span class="sxs-lookup"><span data-stu-id="fc330-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="fc330-112">La capacidad de examinar, buscar o restaurar versiones anteriores de archivos a través de la interfaz de usuario de versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="fc330-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="fc330-113">La capacidad de configurar o programar versiones anteriores de archivos a través de la interfaz de usuario de protección del sistema</span><span class="sxs-lookup"><span data-stu-id="fc330-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="fc330-114">Sin embargo, los usuarios pueden seguir usando la pestaña versiones anteriores al obtener acceso a recursos compartidos de archivos en un servidor Windows.</span><span class="sxs-lookup"><span data-stu-id="fc330-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="fc330-115">Manifestación</span><span class="sxs-lookup"><span data-stu-id="fc330-115">Manifestation</span></span>

<span data-ttu-id="fc330-116">La opción versiones anteriores ya no está disponible para los volúmenes locales en el menú propiedades del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc330-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="fc330-117">Solución</span><span class="sxs-lookup"><span data-stu-id="fc330-117">Solution</span></span>

<span data-ttu-id="fc330-118">Los desarrolladores que necesitan crear instantáneas de volúmenes locales pueden hacerlo mediante una llamada a las API de VSS en código personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc330-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




