---
description: Use el código siguiente para establecer la frecuencia de devolución de llamada.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Establecer la frecuencia de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360372"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="35809-103">Establecer la frecuencia de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="35809-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="35809-104">Use el código siguiente para establecer la frecuencia de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="35809-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="35809-105">**DWORD** Valor = 1;</span><span class="sxs-lookup"><span data-stu-id="35809-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="35809-106">Este fragmento de código establece la frecuencia de devolución de llamada en 1 segundo (el valor mínimo).</span><span class="sxs-lookup"><span data-stu-id="35809-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="35809-107">El valor máximo debe ser mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="35809-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="35809-108">Si el búfer del proveedor de paquetes de red (NPP) está lleno, el NPP vuelve a llamar al monitor antes.</span><span class="sxs-lookup"><span data-stu-id="35809-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



