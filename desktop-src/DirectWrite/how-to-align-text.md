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
# <a name="how-to-align-text"></a><span data-ttu-id="234b3-103">Cómo alinear texto</span><span class="sxs-lookup"><span data-stu-id="234b3-103">How to Align Text</span></span>

<span data-ttu-id="234b3-104">Puede alinear el texto de [DirectWrite](direct-write-portal.md) mediante el método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , como se muestra en el código siguiente que centra el texto.</span><span class="sxs-lookup"><span data-stu-id="234b3-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
}
```



<span data-ttu-id="234b3-105">El texto se puede alinear con el borde inicial o final del cuadro de diseño, o bien se puede centrar.</span><span class="sxs-lookup"><span data-stu-id="234b3-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="234b3-106">En la ilustración siguiente se muestra texto con la alineación establecida en [**DWRITE \_ texto \_ \_ inicial**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), el [**\_ centro de \_ alineación \_ del texto DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)y el final de la [**\_ alineación del texto \_ \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="234b3-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![Ilustración de párrafos de texto con alineación inicial, centrada y final](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="234b3-108">La alineación depende de la dirección de lectura; lo anterior es para la dirección de lectura de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="234b3-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="234b3-109">En la dirección de lectura de derecha a izquierda, sería lo contrario.</span><span class="sxs-lookup"><span data-stu-id="234b3-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="234b3-110">Un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilizará la alineación que se ha designado para el [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) proporcionado por el usuario al crear el diseño.</span><span class="sxs-lookup"><span data-stu-id="234b3-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="234b3-111">Para cambiar la alineación del texto, use [**IDWriteTextLayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span><span class="sxs-lookup"><span data-stu-id="234b3-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 