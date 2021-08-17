---
title: Recuperar atributos de objeto y seleccionar nuevos objetos
description: Una aplicación puede recuperar los atributos de un lápiz, pincel, paleta, fuente o mapa de bits llamando a las funciones GetCurrentObject y GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c58d946f61a6a83dcfeb2ddae24d735d3596e5e864cf672bab832d7db3aedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886156"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Recuperar atributos de objeto y seleccionar nuevos objetos

Una aplicación puede recuperar los atributos de un lápiz, pincel, paleta, fuente o mapa de bits llamando a las funciones [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**y GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) La **función GetCurrentObject** devuelve un identificador que identifica el objeto seleccionado actualmente en el controlador de dominio; La **función GetObject** devuelve una estructura que describe los atributos del objeto .

En el ejemplo siguiente se muestra cómo una aplicación puede recuperar los atributos de pincel actuales y usar los datos recuperados para determinar si es necesario seleccionar un nuevo pincel.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> La aplicación guardó el identificador de pincel original al llamar a la [**función SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) la primera vez. Este identificador se guarda para que el pincel original se pueda volver a seleccionar en el controlador de dominio una vez completada la última operación de dibujo con el nuevo pincel. Después de volver a seleccionar el pincel original en el controlador de dominio, se elimina el nuevo pincel, lo que libera memoria en el montón GDI.

 

 

 



