---
title: Interfaces NDF
description: Las siguientes interfaces se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074995"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="8fc7b-103">Interfaces NDF</span><span class="sxs-lookup"><span data-stu-id="8fc7b-103">NDF Interfaces</span></span>

<span data-ttu-id="8fc7b-104">Las siguientes interfaces se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="8fc7b-105">Aunque esta funcionalidad no es necesaria para la mayoría de las aplicaciones, puede proporcionar diagnósticos y resoluciones más específicos en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="8fc7b-106">Estas interfaces y sus métodos asociados son para desarrolladores que implementan sus propias clases auxiliares de terceros que amplían la funcionalidad NDF.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="8fc7b-107">Nombre de la interfaz</span><span class="sxs-lookup"><span data-stu-id="8fc7b-107">Interface Name</span></span>                                                 | <span data-ttu-id="8fc7b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fc7b-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fc7b-109">**INetDiagHelper**</span><span class="sxs-lookup"><span data-stu-id="8fc7b-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="8fc7b-110">Lo llama el NDF para la mayoría de las actividades que se producen durante un diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="8fc7b-111">**INetDiagHelperEx**</span><span class="sxs-lookup"><span data-stu-id="8fc7b-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="8fc7b-112">Lo llama el NDF para capturar y proporcionar información asociada con los diagnósticos y la resolución de problemas relacionados con la red.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="8fc7b-113">**INetDiagHelperInfo**</span><span class="sxs-lookup"><span data-stu-id="8fc7b-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="8fc7b-114">Lo llama el NDF para validar que tiene información necesaria</span><span class="sxs-lookup"><span data-stu-id="8fc7b-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="8fc7b-115">**INetDiagHelperUtilFactory**</span><span class="sxs-lookup"><span data-stu-id="8fc7b-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="8fc7b-116">Reservado para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="8fc7b-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 




