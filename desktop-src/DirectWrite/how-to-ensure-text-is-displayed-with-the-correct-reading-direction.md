---
title: Asegurarse de que el texto se muestra con la dirección de lectura correcta
description: Algunos idiomas, como el árabe y el hebreo, requieren una dirección de lectura de derecha a izquierda.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793779"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Asegurarse de que el texto se muestra con la dirección de lectura correcta

Algunos idiomas, como el árabe y el hebreo, requieren una dirección de lectura de derecha a izquierda. En el caso de un objeto de formato de texto [DirectWrite](direct-write-portal.md) , la dirección de lectura predeterminada es de izquierda a derecha. DirectWrite no infiere automáticamente la dirección de lectura de la configuración regional, por lo que debe hacerlo usted mismo.

En primer lugar, obtenga las marcas de estilo extendido para la ventana en la que se representará el texto mediante la macro GetWindowStyleEx definida en windowsx. h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



La macro devuelve un valor DWORD compuesto por varias marcas combinadas con operaciones OR bit a bit. Debe determinar si existen las marcas específicas que afectan a la dirección de lectura.

Hay dos marcas diferentes que están relacionadas con la dirección de lectura: WS \_ ex \_ LAYOUTRTL y WS \_ ex \_ RTLREADING.

Use el operador and bit a bit (&) con la variable dwStyle y \_ la \_ macro WS ex LAYOUTRTL para almacenar un valor booleano que indica si el diseño está reflejado.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Haga lo mismo para la marca WS \_ ex \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Establezca la dirección de lectura mediante el método [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) . El valor predeterminado es de izquierda a derecha, por lo que solo tiene que establecer la dirección de lectura si es de derecha a izquierda.

> [!Note]  
> WS \_ ex \_ LAYOUTRTL refleja el diseño completo e implica la dirección de lectura de derecha a izquierda, por lo que debe establecer la dirección de lectura solo si una de estas marcas está presente. Si ambos están presentes, se cancelan entre sí y la dirección de lectura para el formato de texto debe ser de izquierda a derecha.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
