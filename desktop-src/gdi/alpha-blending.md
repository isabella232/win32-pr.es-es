---
description: La combinación alfa se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alpha Blending (GDI de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4add2aca8ac4e2d7e1b24988eb5d40f80bac259c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120290"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="c58eb-103">Alpha Blending (GDI de Windows)</span><span class="sxs-lookup"><span data-stu-id="c58eb-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="c58eb-104">*La combinación alfa* se usa para mostrar un mapa de bits alfa, que es un mapa de bits que tiene píxeles transparentes o semitransparentes.</span><span class="sxs-lookup"><span data-stu-id="c58eb-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="c58eb-105">Además de un canal de color rojo, verde y azul, cada píxel de un mapa de bits alfa tiene un componente de transparencia conocido como *su canal alfa*.</span><span class="sxs-lookup"><span data-stu-id="c58eb-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="c58eb-106">El canal alfa normalmente contiene tantos bits como un canal de color.</span><span class="sxs-lookup"><span data-stu-id="c58eb-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="c58eb-107">Por ejemplo, un canal alfa de 8 bits puede representar 256 niveles de transparencia, de 0 (todo el mapa de bits es transparente) a 255 (todo el mapa de bits es opaco).</span><span class="sxs-lookup"><span data-stu-id="c58eb-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="c58eb-108">Los mecanismos de combinación alfa se invocan mediante una llamada [**a AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), que hace referencia a la [**estructura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)</span><span class="sxs-lookup"><span data-stu-id="c58eb-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="c58eb-109">Los valores alfa por píxel solo se admiten para RGB bi de 32 \_ bpp.</span><span class="sxs-lookup"><span data-stu-id="c58eb-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="c58eb-110">Esta fórmula se define como:</span><span class="sxs-lookup"><span data-stu-id="c58eb-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="c58eb-111">Esto se representa en memoria, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c58eb-111">This is represented in memory as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="c58eb-112">31:24</span><span class="sxs-lookup"><span data-stu-id="c58eb-112">31:24</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-113">23:16</span><span class="sxs-lookup"><span data-stu-id="c58eb-113">23:16</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-114">15:08</span><span class="sxs-lookup"><span data-stu-id="c58eb-114">15:08</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-115">07:00</span><span class="sxs-lookup"><span data-stu-id="c58eb-115">07:00</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="c58eb-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="c58eb-116">Alpha</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-117">Rojo</span><span class="sxs-lookup"><span data-stu-id="c58eb-117">Red</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-118">Verde</span><span class="sxs-lookup"><span data-stu-id="c58eb-118">Green</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c58eb-119">Azul</span><span class="sxs-lookup"><span data-stu-id="c58eb-119">Blue</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="c58eb-120">Los mapas de bits también se pueden mostrar con un factor de transparencia aplicado a todo el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c58eb-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="c58eb-121">Cualquier formato de mapa de bits se puede mostrar con un valor alfa constante global estableciendo **SourceConstantAlpha** en la [**estructura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)</span><span class="sxs-lookup"><span data-stu-id="c58eb-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="c58eb-122">El valor alfa constante global tiene 256 niveles de transparencia, de 0 (todo el mapa de bits es completamente transparente) a 255 (todo el mapa de bits es completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="c58eb-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="c58eb-123">El valor alfa constante global se combina con el valor alfa por píxel.</span><span class="sxs-lookup"><span data-stu-id="c58eb-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="c58eb-124">Para obtener un ejemplo, vea [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="c58eb-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



