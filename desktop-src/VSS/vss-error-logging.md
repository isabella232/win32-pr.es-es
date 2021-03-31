---
description: 'La siguiente información de error y estado de VSS se escribe en el registro de eventos de la aplicación:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registro de errores de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154336"
---
# <a name="vss-error-logging"></a><span data-ttu-id="86070-103">Registro de errores de VSS</span><span class="sxs-lookup"><span data-stu-id="86070-103">VSS Error Logging</span></span>

<span data-ttu-id="86070-104">La siguiente información de error y estado de VSS se escribe en el registro de eventos de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="86070-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="86070-105">Errores del solicitante generados mediante la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="86070-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="86070-106">Los errores de escritura producidos en mediante la clase [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , incluidos los métodos de invalidación</span><span class="sxs-lookup"><span data-stu-id="86070-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="86070-107">Errores generados por el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="86070-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="86070-108">Errores del servicio VSS generados en la coordinación de la actividad de proveedor, escritor y solicitante (por ejemplo, la generación de eventos)</span><span class="sxs-lookup"><span data-stu-id="86070-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="86070-109">Estos errores pueden tener varias causas, incluido un error de programación en código de terceros o errores de configuración relacionados con VSS.</span><span class="sxs-lookup"><span data-stu-id="86070-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="86070-110">Los controladores VSS y la funcionalidad de implementación de nivel inferior escriben errores en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="86070-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="86070-111">El software de terceros (solicitante, proveedor, redactor) puede elegir el registro de la aplicación, el registro del sistema, o ambos, para escribir entradas del registro de errores.</span><span class="sxs-lookup"><span data-stu-id="86070-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="86070-112">Se recomienda que las aplicaciones de alto nivel (como el código en modo de usuario) utilicen el registro de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="86070-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="86070-113">Las aplicaciones de nivel inferior, como las interfaces de hardware y los controladores, deben utilizar el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="86070-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



