---
title: Identificadores de formato
description: Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356989"
---
# <a name="format-identifiers"></a><span data-ttu-id="e38a6-104">Identificadores de formato</span><span class="sxs-lookup"><span data-stu-id="e38a6-104">Format Identifiers</span></span>

<span data-ttu-id="e38a6-105">Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único.</span><span class="sxs-lookup"><span data-stu-id="e38a6-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="e38a6-106">Por ejemplo, FMTID para el conjunto de propiedades de información de Resumen de COM es **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="e38a6-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="e38a6-107">Para definir un FMTID para el conjunto de propiedades de información de Resumen, use la macro **definir \_ GUID** en un archivo de inclusión para el código que manipula el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e38a6-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="e38a6-108">Cualquier código que requiera el valor de FMTID para el conjunto de propiedades de información de resumen puede acceder a él a través de la variable *\_ SummaryInformation de FMTID* .</span><span class="sxs-lookup"><span data-stu-id="e38a6-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="e38a6-109">Al almacenar conjuntos de propiedades en instancias de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , convierta FMTID en un nombre de cadena para el objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="e38a6-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




