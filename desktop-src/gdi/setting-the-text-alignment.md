---
description: Puede consultar y establecer la alineación del texto para un contexto de dispositivo mediante las funciones GetTextAlign y SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Establecer la alineación del texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985383"
---
# <a name="setting-the-text-alignment"></a>Establecer la alineación del texto

Puede consultar y establecer la alineación del texto para un contexto de dispositivo mediante las funciones [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) y [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) . La configuración de la alineación de texto determina cómo se coloca el texto en relación con una ubicación especificada. El texto se puede alinear a la derecha o a la izquierda de la posición o centrarse sobre él; también se puede alinear por encima o por debajo del punto.

En el ejemplo siguiente se muestra un método para determinar qué marca de alineación horizontal se establece:


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



También puede usar la función [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para actualizar la posición actual cuando se llama a una función de salida de texto. Por ejemplo, en el ejemplo siguiente se usa la función [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) para actualizar la posición actual cuando se llama a la función [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . En este ejemplo, el parámetro *cArial* es un entero que especifica el número de fuentes Arial.


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> No debe utilizar [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) con TA \_ UPDATECP cuando esté usando [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), ya que el texto seleccionado no se representa correctamente. Si debe usar esta marca, puede desactivar y restablecerla según sea necesario para evitar el problema.

 

 

 
