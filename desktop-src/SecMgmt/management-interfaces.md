---
description: Enumera las interfaces proporcionadas por el motor de datos adjuntos.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688249"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="ac1f9-103">Interfaces de administración de seguridad</span><span class="sxs-lookup"><span data-stu-id="ac1f9-103">Security Management Interfaces</span></span>

<span data-ttu-id="ac1f9-104">Esta sección contiene páginas de referencia para los siguientes grupos de interfaces:</span><span class="sxs-lookup"><span data-stu-id="ac1f9-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="ac1f9-105">Interfaces del motor de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="ac1f9-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="ac1f9-106">Interfaces del motor de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="ac1f9-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="ac1f9-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ac1f9-107">Interface</span></span>                                                            | <span data-ttu-id="ac1f9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac1f9-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac1f9-109">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="ac1f9-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="ac1f9-110">Recupera datos de configuración y análisis sobre un servicio de seguridad especificado de los complementos de configuración de seguridad. Los complementos de configuración de seguridad exponen esta interfaz, que las extensiones de complemento de datos adjuntos llaman a la información de configuración o análisis de consulta.</span><span class="sxs-lookup"><span data-stu-id="ac1f9-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="ac1f9-111">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="ac1f9-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="ac1f9-112">Recupera información de configuración o análisis modificada de un complemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac1f9-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="ac1f9-113">Los complementos de configuración de seguridad llaman a esta interfaz para recuperar cualquier información modificada de la extensión del complemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ac1f9-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="ac1f9-114">A continuación, el complemento configuración de seguridad almacena estos datos de forma adecuada en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ac1f9-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="ac1f9-115">Para obtener más información sobre las interfaces COM que se deben implementar mediante extensiones de complemento, consulte la documentación de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="ac1f9-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
