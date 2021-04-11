---
description: Se pueden utilizar las siguientes interfaces para recuperar información acerca de los proveedores de servicios criptográficos.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfaces de proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154733"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="45247-103">Interfaces de proveedor de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="45247-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="45247-104">Se pueden utilizar las siguientes interfaces para recuperar información acerca de los proveedores de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="45247-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="45247-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="45247-105">Interface</span></span>                                    | <span data-ttu-id="45247-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="45247-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="45247-107">**ICspAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="45247-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="45247-108">Representa un algoritmo implementado por un proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="45247-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="45247-109">**ICspAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="45247-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="45247-110">Administra una colección de objetos [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="45247-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="45247-111">**ICspInformation**</span><span class="sxs-lookup"><span data-stu-id="45247-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="45247-112">Proporciona acceso a información general sobre un proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="45247-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="45247-113">**ICspInformations**</span><span class="sxs-lookup"><span data-stu-id="45247-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="45247-114">Administra una colección de objetos [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .</span><span class="sxs-lookup"><span data-stu-id="45247-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="45247-115">**ICspStatus**</span><span class="sxs-lookup"><span data-stu-id="45247-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="45247-116">Contiene información sobre un par de algoritmo o proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="45247-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="45247-117">**ICspStatuses**</span><span class="sxs-lookup"><span data-stu-id="45247-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="45247-118">Administra una colección de objetos [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .</span><span class="sxs-lookup"><span data-stu-id="45247-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="45247-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45247-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45247-120">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="45247-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



