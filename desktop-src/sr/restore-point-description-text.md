---
title: Texto de descripción de punto de restauración
description: Cuando una aplicación llama a la función SRSetRestorePoint, puede proporcionar cualquier texto como una descripción para el punto de restauración; sin embargo, en la siguiente tabla se muestra el texto de Descripción recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268877"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="7479d-103">Texto de descripción de punto de restauración</span><span class="sxs-lookup"><span data-stu-id="7479d-103">Restore Point Description Text</span></span>

<span data-ttu-id="7479d-104">Cuando una aplicación llama a la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , puede proporcionar cualquier texto como una descripción para el punto de restauración; sin embargo, en la siguiente tabla se muestra el texto de Descripción recomendado.</span><span class="sxs-lookup"><span data-stu-id="7479d-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="7479d-105">Modificación del sistema</span><span class="sxs-lookup"><span data-stu-id="7479d-105">System modification</span></span>                            | <span data-ttu-id="7479d-106">Tipo de punto de restauración</span><span class="sxs-lookup"><span data-stu-id="7479d-106">Restore point type</span></span>      | <span data-ttu-id="7479d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7479d-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="7479d-108">Instalación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7479d-108">Application installation</span></span>                       | <span data-ttu-id="7479d-109">instalación de la aplicación \_</span><span class="sxs-lookup"><span data-stu-id="7479d-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="7479d-110">Se instaló *appname*</span><span class="sxs-lookup"><span data-stu-id="7479d-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="7479d-111">Modificación de aplicaciones (agregar o quitar características)</span><span class="sxs-lookup"><span data-stu-id="7479d-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="7479d-112">MODIFICAR \_ configuración</span><span class="sxs-lookup"><span data-stu-id="7479d-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="7479d-113">*Nombreaplicación* configurado</span><span class="sxs-lookup"><span data-stu-id="7479d-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="7479d-114">Eliminación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7479d-114">Application removal</span></span>                            | <span data-ttu-id="7479d-115">desinstalación de la aplicación \_</span><span class="sxs-lookup"><span data-stu-id="7479d-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="7479d-116">Se quitó *appname*</span><span class="sxs-lookup"><span data-stu-id="7479d-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="7479d-117">Instalación del controlador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7479d-117">Device driver installation</span></span>                     | <span data-ttu-id="7479d-118">\_instalación del controlador de dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="7479d-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="7479d-119">Instalado *drivername*</span><span class="sxs-lookup"><span data-stu-id="7479d-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="7479d-120">Los instaladores, como Windows Installer e InstallShield, usan estas convenciones para el texto descriptivo:</span><span class="sxs-lookup"><span data-stu-id="7479d-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="7479d-121">El nombre del producto sigue el verbo; por ejemplo, instalado *appname*.</span><span class="sxs-lookup"><span data-stu-id="7479d-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="7479d-122">El nombre de producto se puede usar solo (*appname*) o el nombre del producto y el nombre de la empresa se pueden usar (*MyCompany appname*).</span><span class="sxs-lookup"><span data-stu-id="7479d-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




