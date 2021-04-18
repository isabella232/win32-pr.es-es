---
description: Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar la configuración específica del servicio.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Crear una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688028"
---
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="10b15-103">Crear una extensión de complemento de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="10b15-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="10b15-104">Una extensión de complemento de datos adjuntos proporciona una interfaz que los usuarios pueden usar para cambiar la configuración específica del servicio.</span><span class="sxs-lookup"><span data-stu-id="10b15-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="10b15-105">La extensión del complemento de datos adjuntos debe cumplir los requisitos de MMC para ser una extensión de complemento válida.</span><span class="sxs-lookup"><span data-stu-id="10b15-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="10b15-106">Para obtener más información sobre estos requisitos, consulte la documentación de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="10b15-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="10b15-107">Además de las interfaces requeridas por MMC, una extensión de complemento de datos adjuntos debe implementar la interfaz COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="10b15-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="10b15-108">Los complementos de configuración de seguridad llaman a los métodos de esta interfaz para determinar si los datos de configuración han cambiado y, en caso afirmativo, actualizar la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10b15-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="10b15-109">El complemento de datos adjuntos debe almacenar los cambios de configuración hasta que los complementos de configuración de seguridad recuperen los datos.</span><span class="sxs-lookup"><span data-stu-id="10b15-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="10b15-110">Una extensión de complemento de datos adjuntos debe proporcionar la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="10b15-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="10b15-111">Mostrar información de configuración y análisis</span><span class="sxs-lookup"><span data-stu-id="10b15-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="10b15-112">Modificar la información de configuración en la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="10b15-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="10b15-113">Modificar la información de configuración en la base de datos de seguridad</span><span class="sxs-lookup"><span data-stu-id="10b15-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="10b15-114">Para ayudar a la extensión del complemento a realizar estas tareas, los complementos de configuración de seguridad implementan una interfaz COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que proporciona métodos a los que puede llamar la extensión del complemento para inicializarse y consultar información de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10b15-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="10b15-115">Después de crear la extensión del complemento de datos adjuntos, debe registrarla con los complementos de configuración de seguridad, tal y como se describe en [registrar una extensión de complemento de datos adjuntos](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="10b15-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 
