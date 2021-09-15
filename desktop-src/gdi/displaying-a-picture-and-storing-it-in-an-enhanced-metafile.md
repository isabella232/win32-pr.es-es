---
description: Esta sección contiene un ejemplo que muestra la creación de una imagen y el proceso de almacenamiento de los registros correspondientes en un metarchivo.
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: Mostrar una imagen y almacenarla en un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581129"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a>Mostrar una imagen y almacenarla en un metarchivo mejorado

Esta sección contiene un ejemplo que muestra la creación de una imagen y el proceso de almacenamiento de los registros correspondientes en un metarchivo. En el ejemplo se dibuja una imagen en la pantalla o se almacena en un metarchivo. Si se da un identificador de contexto de dispositivo de presentación, dibuja una imagen en la pantalla mediante varias funciones GDI. Si se proporciona un contexto de dispositivo de metarchivo mejorado, almacena la misma imagen en el metarchivo mejorado.


```C++
void DrawOrStore(HWND hwnd, HDC hdcMeta, HDC hdcDisplay) 
{ 
 
RECT rect; 
HDC hDC; 
int fnMapModeOld; 
HBRUSH hbrOld; 
 
// Draw it to the display DC or store it in the metafile device context.  
 
if (hdcMeta) 
    hDC = hdcMeta; 
else 
    hDC = hdcDisplay; 
 
// Set the mapping mode in the device context.  
 
fnMapModeOld = SetMapMode(hDC, MM_LOENGLISH); 
 
// Find the midpoint of the client area.  
 
GetClientRect(hwnd, (LPRECT)&rect); 
DPtoLP(hDC, (LPPOINT)&rect, 2); 
 
// Select a gray brush.  
 
hbrOld = SelectObject(hDC, GetStockObject(GRAY_BRUSH)); 
 
// Draw a circle with a one inch radius.  
 
Ellipse(hDC, (rect.right/2 - 100), (rect.bottom/2 + 100), 
       (rect.right/2 + 100), (rect.bottom/2 - 100)); 
 
// Perform additional drawing here.  
 
 
 
// Set the device context back to its original state.  
 
SetMapMode(hDC, fnMapModeOld); 
SelectObject(hDC, hbrOld); 
} 
```



 

 



