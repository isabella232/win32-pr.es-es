---
title: CPROVCF. CPP
description: En el componente proveedor de ejemplo, un ejemplo de código del código del generador de clases de objetos del proveedor de ADs está en cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486570"
---
# <a name="cprovcfcpp"></a><span data-ttu-id="ad518-103">CPROVCF. CPP</span><span class="sxs-lookup"><span data-stu-id="ad518-103">CPROVCF.CPP</span></span>

<span data-ttu-id="ad518-104">En el componente proveedor de ejemplo, un ejemplo de código del código del generador de clases de objetos del proveedor de ADs está en cprovcf. cpp.</span><span class="sxs-lookup"><span data-stu-id="ad518-104">In the example provider component, one code example of the ADs provider object class factory code is in cprovcf.cpp.</span></span> <span data-ttu-id="ad518-105">El componente de proveedor nunca crea directamente una instancia de este objeto en ningún momento distinto de cuando se crea automáticamente el objeto durante las operaciones de enlace en [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o la función interna en el método Visual Basic **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="ad518-105">The provider component never directly creates an instance of this object at any time other than when the object is created automatically during the binding operations in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or the internal function in the Visual Basic method **GetObject**.</span></span> <span data-ttu-id="ad518-106">El método admitido se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ad518-106">The supported method is listed in the following table.</span></span>



| <span data-ttu-id="ad518-107">Método</span><span class="sxs-lookup"><span data-stu-id="ad518-107">Method</span></span>                                  | <span data-ttu-id="ad518-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad518-108">Description</span></span>                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ad518-109">**CSampleDSProviderCF:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ad518-109">**CSampleDSProviderCF::CreateInstance**</span></span> | <span data-ttu-id="ad518-110">Crea una instancia del generador de clases para el objeto de proveedor de ADS.</span><span class="sxs-lookup"><span data-stu-id="ad518-110">Creates an instance of the class factory for the ADS provider object.</span></span> |



 

 

 




