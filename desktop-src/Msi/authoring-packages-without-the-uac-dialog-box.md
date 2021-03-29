---
description: Cuando no se necesitan privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete puede suprimir el cuadro de diálogo que muestra el control de cuentas de usuario (UAC) para solicitar a los usuarios la autorización de administrador.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Crear paquetes sin el cuadro de diálogo UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813331"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="27b0b-103">Crear paquetes sin el cuadro de diálogo UAC</span><span class="sxs-lookup"><span data-stu-id="27b0b-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="27b0b-104">Cuando no se necesitan privilegios elevados para instalar un paquete de Windows Installer, el autor del paquete puede suprimir el cuadro de diálogo que muestra el [*control de cuentas de usuario*](u-gly.md) (UAC) para solicitar a los usuarios la autorización de administrador.</span><span class="sxs-lookup"><span data-stu-id="27b0b-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="27b0b-105">Para suprimir la presentación del cuadro de diálogo de UAC al instalar la aplicación, el autor del paquete debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="27b0b-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="27b0b-106">Instale la aplicación mediante el instalador de Windows 4,0 o posterior en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27b0b-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="27b0b-107">No dependa de usar privilegios del sistema elevados para instalar la aplicación en el equipo.</span><span class="sxs-lookup"><span data-stu-id="27b0b-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="27b0b-108">Instale la aplicación en el contexto por usuario y haga que este sea el contexto de instalación predeterminado del paquete.</span><span class="sxs-lookup"><span data-stu-id="27b0b-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="27b0b-109">Si no se establece la propiedad [**AllUsers**](allusers.md) , el instalador instala el paquete en el contexto por usuario.</span><span class="sxs-lookup"><span data-stu-id="27b0b-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="27b0b-110">Si no incluye la propiedad **AllUsers** en la tabla de [propiedades](property-table.md), el instalador no establece esta propiedad y, por tanto, la instalación por usuario se convierte en el contexto de instalación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27b0b-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="27b0b-111">Puede invalidar este valor predeterminado estableciendo la propiedad **AllUsers** en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="27b0b-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="27b0b-112">Establezca bit 3 en la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) para indicar que no se necesitan privilegios elevados para instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27b0b-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



