---
description: Tengo un archivo AVI que contiene una secuencia de Windows Media Video.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Tengo un archivo AVI que contiene una secuencia de Windows Media Video. ¿Cómo puedo convertirlo en un archivo WMV?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707523"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="d42ec-104">Tengo un archivo AVI que contiene una secuencia de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="d42ec-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="d42ec-105">¿Cómo puedo convertirlo en un archivo WMV?</span><span class="sxs-lookup"><span data-stu-id="d42ec-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="d42ec-106">Las interfaces de códec de Windows Media Audio y vídeo no proporcionan métodos para crear archivos con el formato de sistemas avanzados (ASF), que es el formato que se usa para los archivos WMV.</span><span class="sxs-lookup"><span data-stu-id="d42ec-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="d42ec-107">Si desea convertir un archivo (con cualquier contenedor) en un archivo ASF, debe utilizar los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d42ec-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="d42ec-108">Recupere los ejemplos comprimidos de Windows Media del archivo de origen y páselo al objeto escritor como ejemplos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="d42ec-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="d42ec-109">Para obtener más información, consulte la documentación del SDK de Windows Media Format 9 series.</span><span class="sxs-lookup"><span data-stu-id="d42ec-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d42ec-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d42ec-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d42ec-111">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="d42ec-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



