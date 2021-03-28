---
description: Puede determinar el número de colores que admite un dispositivo y cuáles son los colores mediante la recuperación del recuento de colores del dispositivo y la enumeración de los colores de los lápices sólidos.
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: Enumerar colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984967"
---
# <a name="enumerating-colors"></a>Enumerar colores

Puede determinar el número de colores que admite un dispositivo y cuáles son los colores mediante la recuperación del recuento de colores del dispositivo y la enumeración de los colores de los lápices sólidos. Para recuperar el número de colores, utilice la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) con el valor NUMCOLORS. Para enumerar lápices sólidos, utilice la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) y una función de devolución de llamada correspondiente que reciba información sobre cada lápiz.


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 



