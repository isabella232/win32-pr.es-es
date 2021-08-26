---
title: Asegúrese de que el texto se muestra con la dirección de lectura correcta.
description: Algunos idiomas, como árabe y hebreo, requieren una dirección de lectura de derecha a izquierda.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982175"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Asegúrese de que el texto se muestra con la dirección de lectura correcta.

Algunos idiomas, como árabe y hebreo, requieren una dirección de lectura de derecha a izquierda. Para un [DirectWrite](direct-write-portal.md) de formato de texto, la dirección de lectura predeterminada es de izquierda a derecha. DirectWrite no deduce automáticamente la dirección de lectura de la configuración regional, por lo que debe hacerlo usted mismo.

En primer lugar, obtenga las marcas de estilo extendidas para la ventana en la que se representará el texto mediante la macro GetWindowStyleEx definida en windowsx.h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



La macro devuelve un valor DWORD que se forma con varias marcas combinadas con operaciones OR bit a bit. Debe determinar si las marcas específicas que afectan a la dirección de lectura están ahí.

Hay dos marcas diferentes relacionadas con la dirección de lectura: WS \_ EX \_ LAYOUTRTL y WS \_ EX \_ RTLREADING.

Use el operador AND bit a bit (&) con la variable dwStyle y la macro LAYOUTRTL de WS EX para almacenar un valor BOOL que indica si el diseño está \_ \_ reflejado.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Haga lo mismo con la marca WS \_ EX \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Establezca la dirección de lectura mediante el [**método IDWriteTextFormat::SetReadingDirection.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) El valor predeterminado es de izquierda a derecha, por lo que solo debe establecer la dirección de lectura si es de derecha a izquierda.

> [!Note]  
> WS \_ EX LAYOUTRTL refleja todo el diseño e implica la dirección de lectura de derecha a izquierda, por lo que establezca la dirección de lectura solo si una de estas marcas \_ está presente. Si ambos están presentes, se cancelan entre sí y la dirección de lectura del formato de texto debe ser de izquierda a derecha.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
