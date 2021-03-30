---
title: Cómo alinear texto
description: Puede alinear el texto de DirectWrite mediante el método SetTextAlignment de la interfaz IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfd7a025769dea34444236805ebb8e5530ea06c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792664"
---
# <a name="how-to-align-text"></a>Cómo alinear texto

Puede alinear el texto de [DirectWrite](direct-write-portal.md) mediante el método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , como se muestra en el código siguiente que centra el texto.


```C++
if (SUCCEEDED(hr))
{
    hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
}
```



El texto se puede alinear con el borde inicial o final del cuadro de diseño, o bien se puede centrar. En la ilustración siguiente se muestra texto con la alineación establecida en [**DWRITE \_ texto \_ \_ inicial**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), el [**\_ centro de \_ alineación \_ del texto DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)y el final de la [**\_ alineación del texto \_ \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.

![Ilustración de párrafos de texto con alineación inicial, centrada y final](images/textalignment.png)

> [!Note]  
> La alineación depende de la dirección de lectura; lo anterior es para la dirección de lectura de izquierda a derecha. En la dirección de lectura de derecha a izquierda, sería lo contrario.

 

Un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilizará la alineación que se ha designado para el [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) proporcionado por el usuario al crear el diseño. Para cambiar la alineación del texto, use [**IDWriteTextLayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 