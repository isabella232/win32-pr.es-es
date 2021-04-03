---
description: La interfaz IUpdateInstaller define las siguientes propiedades.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propiedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908063"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="f0552-103">Propiedades de IUpdateInstaller</span><span class="sxs-lookup"><span data-stu-id="f0552-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="f0552-104">La interfaz [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0552-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="f0552-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f0552-105">Property</span></span>                                                                                      | <span data-ttu-id="f0552-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0552-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0552-107">**AllowSourcePrompts**</span><span class="sxs-lookup"><span data-stu-id="f0552-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="f0552-108">Obtiene y establece un valor booleano que indica si se van a mostrar mensajes de origen al usuario al instalar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="f0552-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="f0552-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="f0552-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="f0552-110">Obtiene y establece la aplicación cliente actual.</span><span class="sxs-lookup"><span data-stu-id="f0552-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="f0552-111">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="f0552-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="f0552-112">Obtiene un valor booleano que indica si una instalación o desinstalación está en curso en un equipo en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="f0552-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="f0552-113">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="f0552-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="f0552-114">Obtiene o establece un valor booleano que indica si se va a instalar o desinstalar forzosamente una actualización.</span><span class="sxs-lookup"><span data-stu-id="f0552-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="f0552-115">**ParentHwnd**</span><span class="sxs-lookup"><span data-stu-id="f0552-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="f0552-116">Obtiene y establece un identificador para la ventana primaria que puede contener un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f0552-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="f0552-117">**ParentWindow**</span><span class="sxs-lookup"><span data-stu-id="f0552-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="f0552-118">Obtiene y establece la interfaz que representa la ventana primaria que puede contener un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f0552-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="f0552-119">**RebootRequiredBeforeInstallation**</span><span class="sxs-lookup"><span data-stu-id="f0552-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="f0552-120">Obtiene un valor booleano que indica si es necesario reiniciar el sistema antes de instalar o desinstalar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="f0552-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="f0552-121">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="f0552-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="f0552-122">Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican para la instalación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="f0552-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



