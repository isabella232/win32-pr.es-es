---
description: Cómo descomprimir secuencias desde un archivo AVI u otro archivo sobre el que no tengo información de formato?
ms.assetid: 980f52f4-17a4-4871-9269-f9e0b97416c6
title: Cómo descomprimir secuencias desde un archivo AVI u otro archivo sobre el que no tengo información de formato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad230c36097a93b3d2d41ddffb35600d0616ea5f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717357"
---
# <a name="how-do-i-decompress-streams-from-an-avi-file-or-other-file-about-which-i-have-no-format-information"></a><span data-ttu-id="93043-103">Cómo descomprimir secuencias desde un archivo AVI u otro archivo sobre el que no tengo información de formato?</span><span class="sxs-lookup"><span data-stu-id="93043-103">How do I decompress streams from an AVI file or other file about which I have no format information?</span></span>

<span data-ttu-id="93043-104">Sin la información de formato, incluidos los datos de formato extendido, no se pueden descomprimir los datos codificados con un códec de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93043-104">Without format information, including extended format data, you cannot decompress data that was encoded with a Windows Media codec.</span></span> <span data-ttu-id="93043-105">Los códecs se diseñaron para crear secuencias de datos para su uso con el contenedor de archivos Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="93043-105">The codecs were designed to create data streams for use with the Advanced Systems Format (ASF) file container.</span></span> <span data-ttu-id="93043-106">La sección de encabezado de un archivo ASF almacena la información de formato de todas las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="93043-106">The header section of an ASF file stores the format information for all of the streams in the file.</span></span> <span data-ttu-id="93043-107">Al usar el contenido codificado mediante uno de los códecs de Windows Media Audio y vídeo fuera de un archivo ASF, debe asegurarse de que la información de formato está disponible.</span><span class="sxs-lookup"><span data-stu-id="93043-107">When you use content encoded using one of the Windows Media Audio and Video codecs outside of an ASF file, you must ensure that the format information is available.</span></span> <span data-ttu-id="93043-108">La manera de hacerlo varía de un contenedor a otro.</span><span class="sxs-lookup"><span data-stu-id="93043-108">The way to do this varies from one container to another.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93043-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93043-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93043-110">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="93043-110">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



