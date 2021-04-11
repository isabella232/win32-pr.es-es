---
description: La interfaz IUpdateInstallationResult define las siguientes propiedades.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propiedades de IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275536"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="43378-103">Propiedades de IUpdateInstallationResult</span><span class="sxs-lookup"><span data-stu-id="43378-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="43378-104">La interfaz [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="43378-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="43378-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43378-105">Property</span></span>                                                           | <span data-ttu-id="43378-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="43378-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43378-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="43378-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="43378-108">Obtiene el valor de excepción **HRESULT** que se genera durante la operación en una actualización.</span><span class="sxs-lookup"><span data-stu-id="43378-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="43378-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="43378-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="43378-110">Obtiene un valor booleano que indica si se requiere un reinicio del sistema en un equipo para completar la instalación de una actualización.</span><span class="sxs-lookup"><span data-stu-id="43378-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="43378-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="43378-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="43378-112">Obtiene un valor [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.</span><span class="sxs-lookup"><span data-stu-id="43378-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



