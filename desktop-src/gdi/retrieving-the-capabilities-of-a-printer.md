---
description: No todos los dispositivos de salida admiten todo el conjunto de funciones gráficas.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recuperar las funcionalidades de una impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779065"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>Recuperar las funcionalidades de una impresora

No todos los dispositivos de salida admiten todo el conjunto de funciones gráficas. Por ejemplo, debido a las limitaciones de hardware, la mayoría de los trazadores vectoriales no admiten transferencias de bloques de bits. Una aplicación puede determinar si un dispositivo admite una función gráfica determinada llamando a la función [**GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) especificando el índice adecuado y examinando el valor devuelto.

En el ejemplo siguiente se muestra cómo una aplicación prueba una impresora para determinar si admite transferencias de bloques de bits.


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



 

 



