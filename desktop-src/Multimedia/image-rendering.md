---
title: Representación de imágenes
description: Representación de imágenes
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, representación de imágenes
- DrawDib, dibujar DIB
- DrawDibDraw función)
- DrawDibGetBuffer función)
- DrawDibUpdate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076292"
---
# <a name="image-rendering"></a><span data-ttu-id="f74b8-108">Representación de imágenes</span><span class="sxs-lookup"><span data-stu-id="f74b8-108">Image Rendering</span></span>

<span data-ttu-id="f74b8-109">Después de llamar a [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) para crear un controlador de dominio de DrawDib (consulte [operaciones de DrawDib](drawdib-operations.md)), puede dibujar un DIB en la pantalla mediante la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="f74b8-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="f74b8-110">**DrawDibDraw** crea un mapa de bits de color verdadero al mostrarlos con adaptadores de pantalla de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f74b8-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="f74b8-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) también admite compresores de vídeo de forma transparente al mostrar mapas de bits comprimidos.</span><span class="sxs-lookup"><span data-stu-id="f74b8-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="f74b8-112">Puede tener acceso al búfer que contiene la imagen descomprimida mediante la función [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="f74b8-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="f74b8-113">**DrawDibGetBuffer** devuelve **null** cuando se dibuja un mapa de bits sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="f74b8-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="f74b8-114">Debe preparar la aplicación para administrar los mapas de bits comprimidos y sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="f74b8-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="f74b8-115">Puede actualizar una imagen o una parte de una imagen que se muestra en la aplicación mediante la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .</span><span class="sxs-lookup"><span data-stu-id="f74b8-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f74b8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f74b8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f74b8-117">Acerca de las funciones de DrawDib</span><span class="sxs-lookup"><span data-stu-id="f74b8-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




