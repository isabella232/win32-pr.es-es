---
description: WMI no admite actualmente código administrado en WMI, pero sí se admite en MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Crear un cliente WMI administrado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706174"
---
# <a name="creating-a-managed-wmi-client"></a><span data-ttu-id="4cc78-103">Crear un cliente WMI administrado</span><span class="sxs-lookup"><span data-stu-id="4cc78-103">Creating a Managed WMI Client</span></span>

<span data-ttu-id="4cc78-104">La versión actual de WMI contiene el espacio de nombres System. Management, que expone una serie de API que interactúan con WMI.</span><span class="sxs-lookup"><span data-stu-id="4cc78-104">The current release of WMI does contain the System.Management namespace, which exposes a number of API's that interact with WMI.</span></span> <span data-ttu-id="4cc78-105">Sin embargo, no se recomienda usar este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="4cc78-105">However, it is not recommended that you use this namespace.</span></span>

<span data-ttu-id="4cc78-106">Si desea crear un cliente WMI administrado, se recomienda que use la infraestructura de administración de Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="4cc78-106">If you wish to create a managed WMI client, it is recommended that you use the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="4cc78-107">MI es la versión de la próxima generación de WMI y contiene compatibilidad total con el código administrado.</span><span class="sxs-lookup"><span data-stu-id="4cc78-107">MI is the next-generation version of WMI, and contains full support for managed code.</span></span> <span data-ttu-id="4cc78-108">Para obtener más información, vea [cómo implementar un cliente de mi administrado](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span><span class="sxs-lookup"><span data-stu-id="4cc78-108">For more information, see [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span></span>

 

 
