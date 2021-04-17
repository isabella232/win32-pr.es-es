---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 3.0 y versiones anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: No se admite en Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677655"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="05d30-103">No se admite en Windows Installer 3,0</span><span class="sxs-lookup"><span data-stu-id="05d30-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="05d30-104">Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 3,0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="05d30-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="05d30-105">La ausencia de una característica de esta lista no garantiza que se admita la característica.</span><span class="sxs-lookup"><span data-stu-id="05d30-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="05d30-106">Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada.</span><span class="sxs-lookup"><span data-stu-id="05d30-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="05d30-107">Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="05d30-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="05d30-108">Windows Installer 3,0 está disponible para Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="05d30-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="05d30-109">Para obtener una lista de todas las versiones de Windows Installer y redistribuibles, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="05d30-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="05d30-110">Las siguientes características no se admiten en Windows Installer 3,0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="05d30-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="05d30-111">Funciones del instalador</span><span class="sxs-lookup"><span data-stu-id="05d30-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="05d30-112">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="05d30-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="05d30-113">**MsiNotifySidChange**</span><span class="sxs-lookup"><span data-stu-id="05d30-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="05d30-114">Prototipo de función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="05d30-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="05d30-115">**\_registro del controlador de INSTALLUI \_**</span><span class="sxs-lookup"><span data-stu-id="05d30-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="05d30-116">Tablas de base de datos</span><span class="sxs-lookup"><span data-stu-id="05d30-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="05d30-117">La columna valor de la [tabla MsiPatchMetadata](msipatchmetadata-table.md) acepta **OptimizedInstallMode** y **MinorUpdateTargetRTM**.</span><span class="sxs-lookup"><span data-stu-id="05d30-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="05d30-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05d30-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="05d30-119">**Propiedad Msix64**</span><span class="sxs-lookup"><span data-stu-id="05d30-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="05d30-120">Windows Installer en sistemas operativos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="05d30-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="05d30-121">La [**propiedad de Resumen**](template-summary.md) de la plantilla acepta el valor x64.</span><span class="sxs-lookup"><span data-stu-id="05d30-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="05d30-122">Evaluadores de coherencia interna-CIEM</span><span class="sxs-lookup"><span data-stu-id="05d30-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="05d30-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="05d30-123">ICE99</span></span>](ice99.md)

 

 
