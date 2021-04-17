---
description: 'La extensión del complemento de datos adjuntos no tiene ninguna manera de consultar directamente la base de datos de seguridad para recuperar información. En su lugar, debe consultar esta información de los complementos de configuración de seguridad mediante ISceSvcAttachmentData:: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Obtención de datos de los complementos de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546211"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a><span data-ttu-id="8deb2-104">Obtención de datos de los complementos de configuración</span><span class="sxs-lookup"><span data-stu-id="8deb2-104">Getting Data from the Configuration Snap-ins</span></span>

<span data-ttu-id="8deb2-105">La extensión del complemento de datos adjuntos no tiene ninguna manera de consultar directamente la base de datos de seguridad para recuperar información.</span><span class="sxs-lookup"><span data-stu-id="8deb2-105">The attachment snap-in extension has no way to directly query the security database to retrieve information.</span></span> <span data-ttu-id="8deb2-106">En su lugar, debe consultar esta información de los complementos de configuración de seguridad mediante [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="8deb2-106">Instead, it must query this information from the Security Configuration snap-ins using [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

<span data-ttu-id="8deb2-107">El complemento de datos adjuntos puede recuperar todos los datos cuando se inicializa o puede recuperar información cuando se abre su nodo.</span><span class="sxs-lookup"><span data-stu-id="8deb2-107">The attachment snap-in can retrieve all of the data when it initializes itself, or it can retrieve information when its node is opened.</span></span>

> [!Note]  
> <span data-ttu-id="8deb2-108">Debe usar el método [**ISceSvcAttachmentData:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) para liberar el búfer asignado por el método de complemento de configuración de seguridad [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="8deb2-108">You must use the [**ISceSvcAttachmentData::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) method to free the buffer allocated by the Security Configuration snap-in method [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

 

 

 



