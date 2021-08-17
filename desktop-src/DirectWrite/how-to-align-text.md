---
title: Alineación de texto
description: Puede alinear DirectWrite texto mediante el método SetTextAlignment de la interfaz IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650375"
---
# <a name="how-to-align-text"></a>Alineación de texto

Puede alinear [DirectWrite](direct-write-portal.md) texto mediante el método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de la interfaz [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) como se muestra en el código siguiente que centra el texto.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



El texto se puede alinear con el borde inicial o final del cuadro de diseño, o se puede centrar. En la ilustración siguiente se muestra texto con la alineación establecida en [**DWRITE \_ TEXT ALIGNMENT \_ \_ LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE TEXT ALIGNMENT \_ \_ \_ CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)y [**DWRITE TEXT ALIGNMENT \_ \_ \_ TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.

![ilustración de párrafos de texto con alineación inicial, centrada y final](images/textalignment.png)

> [!Note]  
> La alineación depende de la dirección de lectura, la anterior es para la dirección de lectura de izquierda a derecha. Para la dirección de lectura de derecha a izquierda, sería lo contrario.

 

Un [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usará la alineación que se ha designado para [**el IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) proporcionado por usted al crear el diseño. Para cambiar la alineación del texto, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
