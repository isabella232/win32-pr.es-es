---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcadores
- Advanced Systems Format (ASF), marcadores
- ASF (formato de sistemas avanzados), marcadores
- marcadores, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903848"
---
# <a name="markers"></a><span data-ttu-id="ffdf4-107">Marcadores</span><span class="sxs-lookup"><span data-stu-id="ffdf4-107">Markers</span></span>

<span data-ttu-id="ffdf4-108">Los marcadores se denominan lugares en la escala de tiempo de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="ffdf4-109">Cada marcador tiene un nombre y un tiempo de presentación que se asigna.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="ffdf4-110">Puede especificar tantos marcadores como necesite para un archivo.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="ffdf4-111">Los marcadores son útiles para dividir archivos ASF grandes en partes lógicas.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="ffdf4-112">Una aplicación que usa el objeto lector para reproducir archivos ASF puede proporcionar al usuario la opción de omitir de un marcador a un marcador, lo que simplifica la navegación de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="ffdf4-113">Por ejemplo, si va a crear un archivo ASF fuera de una presentación, puede colocar marcadores en la escala de tiempo para cada tema principal que se describe.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="ffdf4-114">En la reproducción, en lugar de obtener una escala de tiempo larga y tener que adivinar en la ubicación en la que se va a buscar, un usuario puede elegir simplemente un tema de una lista y ir directamente a la parte pertinente del archivo.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="ffdf4-115">El objeto editor de metadatos manipula los marcadores.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="ffdf4-116">Puede Agregar, quitar y ver los marcadores de un archivo en cualquier momento después de que se haya escrito el archivo.</span><span class="sxs-lookup"><span data-stu-id="ffdf4-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffdf4-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffdf4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffdf4-118">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="ffdf4-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="ffdf4-119">**Para buscar marcadores**</span><span class="sxs-lookup"><span data-stu-id="ffdf4-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="ffdf4-120">**Usar marcadores**</span><span class="sxs-lookup"><span data-stu-id="ffdf4-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




