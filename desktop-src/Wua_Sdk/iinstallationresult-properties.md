---
description: La interfaz IInstallationResult define las siguientes propiedades.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propiedades de IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082180"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="4affb-103">Propiedades de IInstallationResult</span><span class="sxs-lookup"><span data-stu-id="4affb-103">IInstallationResult Properties</span></span>

<span data-ttu-id="4affb-104">La interfaz [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4affb-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="4affb-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4affb-105">Property</span></span>                                                     | <span data-ttu-id="4affb-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4affb-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4affb-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="4affb-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="4affb-108">Obtiene el **HRESULT** de la excepción, si existe, que se genera durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="4affb-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="4affb-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="4affb-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="4affb-110">Obtiene un valor booleano que indica si se debe reiniciar el equipo para completar la instalación o desinstalación de una actualización.</span><span class="sxs-lookup"><span data-stu-id="4affb-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="4affb-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="4affb-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="4affb-112">Obtiene un valor [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.</span><span class="sxs-lookup"><span data-stu-id="4affb-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



