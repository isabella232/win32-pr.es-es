---
description: No todos los dispositivos de salida admiten el conjunto completo de funciones de gráficos.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recuperación de las capacidades de una impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984810"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="ce0ab-103">Recuperación de las capacidades de una impresora</span><span class="sxs-lookup"><span data-stu-id="ce0ab-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="ce0ab-104">No todos los dispositivos de salida admiten el conjunto completo de funciones de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="ce0ab-105">Por ejemplo, debido a las limitaciones de hardware, la mayoría de los trazadores vectoriales no admiten las transferencias de bloque de bits.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="ce0ab-106">Una aplicación puede determinar si un dispositivo admite una función de gráficos determinada llamando a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando el índice adecuado y examinando el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="ce0ab-107">En el ejemplo siguiente se muestra cómo una aplicación prueba una impresora para determinar si admite transferencias de bloque de bits.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



