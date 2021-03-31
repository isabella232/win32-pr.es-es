---
description: El atributo stretchmode especifica cómo ajustar una imagen que no coincide con las dimensiones de salida.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911702"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="53d75-103">Atributo stretchmode</span><span class="sxs-lookup"><span data-stu-id="53d75-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="53d75-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="53d75-104">\[Deprecated.</span></span> <span data-ttu-id="53d75-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53d75-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53d75-106">El `stretchmode` atributo especifica cómo ajustar una imagen que no coincide con las dimensiones de salida.</span><span class="sxs-lookup"><span data-stu-id="53d75-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="53d75-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="53d75-107">Possible Values</span></span>

<span data-ttu-id="53d75-108">Debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="53d75-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="53d75-109">"stretch": la imagen se ajusta para ajustarse al tamaño del marco de salida sin conservar la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="53d75-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="53d75-110">(Es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="53d75-110">(Default)</span></span>
-   <span data-ttu-id="53d75-111">"recortar": la imagen se recorta para ajustarse al tamaño del marco de salida.</span><span class="sxs-lookup"><span data-stu-id="53d75-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="53d75-112">"PreserveAspectRatio": se conserva la relación de aspecto original, con una panorámica negra a lo largo de la dimensión más corta.</span><span class="sxs-lookup"><span data-stu-id="53d75-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="53d75-113">"preserveaspectrationoletterbox": la imagen cambia de tamaño para rellenar todo el marco de destino conservando la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="53d75-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="53d75-114">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="53d75-114">Applies To</span></span>

[<span data-ttu-id="53d75-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="53d75-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="53d75-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="53d75-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d75-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="53d75-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="53d75-118">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="53d75-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



