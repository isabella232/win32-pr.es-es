---
description: Los desarrolladores pueden impedir que se escriba información confidencial, como contraseñas, en el archivo de registro durante una instalación Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Impedir que se escriba información confidencial en el archivo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082530"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="a6623-103">Impedir que se escriba información confidencial en el archivo de registro</span><span class="sxs-lookup"><span data-stu-id="a6623-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="a6623-104">Al usar el Windows Installer, puede evitar que se escriba información confidencial, por ejemplo contraseñas, en el archivo de registro y se haga visible.</span><span class="sxs-lookup"><span data-stu-id="a6623-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="a6623-105">El instalador nunca escribe en el registro la información de la columna de contraseña de la [tabla ServiceInstall](serviceinstall-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a6623-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="a6623-106">Puede impedir que el instalador escriba la propiedad asociada a un [control de edición](edit-control.md) en el registro estableciendo el atributo de [control de contraseña](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a6623-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="a6623-107">La propiedad asociada a un control de edición que tiene el atributo de control de contraseña está oculta aunque la Directiva de [depuración](debug.md) esté establecida en un valor de 7.</span><span class="sxs-lookup"><span data-stu-id="a6623-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="a6623-108">Puede evitar que el instalador escriba una propiedad privada en el registro incluyendo la propiedad en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a6623-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="a6623-109">Este método puede hacer que la información confidencial especificada en una línea de comandos esté visible en el registro.</span><span class="sxs-lookup"><span data-stu-id="a6623-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="a6623-110">Cuando la Directiva de [depuración](debug.md) está establecida en un valor de 7, el instalador escribe la información especificada en una línea de comandos en el registro.</span><span class="sxs-lookup"><span data-stu-id="a6623-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="a6623-111">Esto hace que la propiedad especificada en una línea de comandos sea visible aunque la propiedad esté incluida en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a6623-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="a6623-112">Puede evitar que la información de la columna target de la tabla [CustomAction](customaction-table.md) se escriba en el registro incluyendo la marca de bits HideTarget en el campo Type de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="a6623-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="a6623-113">El valor de esta marca es 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="a6623-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="a6623-114">Para obtener más información, vea [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="a6623-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



