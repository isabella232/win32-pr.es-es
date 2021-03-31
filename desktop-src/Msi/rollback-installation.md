---
description: Cuando el Windows Installer procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Revertir instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155512"
---
# <a name="rollback-installation"></a><span data-ttu-id="9167d-103">Revertir instalación</span><span class="sxs-lookup"><span data-stu-id="9167d-103">Rollback Installation</span></span>

<span data-ttu-id="9167d-104">Cuando el Windows Installer procesa el script de instalación para la instalación de un producto o aplicación, genera simultáneamente un script de reversión y guarda una copia de todos los archivos eliminados durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="9167d-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="9167d-105">Estos archivos se conservan en un directorio oculto del sistema y se eliminan automáticamente una vez completada correctamente la instalación.</span><span class="sxs-lookup"><span data-stu-id="9167d-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="9167d-106">Si no es así, el instalador realiza automáticamente una instalación de reversión que devuelve el sistema a su estado original.</span><span class="sxs-lookup"><span data-stu-id="9167d-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="9167d-107">La reversión automática de una instalación incorrecta es el comportamiento predeterminado del instalador.</span><span class="sxs-lookup"><span data-stu-id="9167d-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="9167d-108">Para deshabilitar la reversión durante una instalación, use uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9167d-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="9167d-109">**Propiedad DISABLEROLLBACK**</span><span class="sxs-lookup"><span data-stu-id="9167d-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="9167d-110">**Propiedad PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="9167d-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="9167d-111">Acción DisableRollback</span><span class="sxs-lookup"><span data-stu-id="9167d-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="9167d-112">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="9167d-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="9167d-113">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="9167d-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="9167d-114">Cada vez que se deshabilita la reversión, el instalador establece la propiedad [**RollbackDisabled**](rollbackdisabled.md) .</span><span class="sxs-lookup"><span data-stu-id="9167d-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="9167d-115">Si una instalación utiliza [acciones personalizadas](custom-actions.md), se requiere la creación de un paquete de instalación adicional para usar la funcionalidad de reversión.</span><span class="sxs-lookup"><span data-stu-id="9167d-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="9167d-116">Para obtener más información, consulte [reversión de acciones personalizadas](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9167d-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



