---
title: Sección marquesina
description: Sección marquesina
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- crear máscaras, sección marquesina
- escribir código para máscaras, sección marquesina
- marquesinas en máscaras, sección de marquesina
- archivos de definición de máscara, sección de marquesina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780053"
---
# <a name="marquee-section"></a><span data-ttu-id="eac56-109">Sección marquesina</span><span class="sxs-lookup"><span data-stu-id="eac56-109">Marquee Section</span></span>

<span data-ttu-id="eac56-110">La sección marquesina contiene información sobre el cuadro de texto marquesina, que mostrará el texto desplazado:</span><span class="sxs-lookup"><span data-stu-id="eac56-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="eac56-111">Esto mostrará el título y el autor del elemento multimedia actual, aunque puede mostrar cualquier tipo de texto en la marquesina.</span><span class="sxs-lookup"><span data-stu-id="eac56-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="eac56-112">Por ejemplo, también puede incluir el nombre de archivo, el estado y la lista de reproducción en el marco.</span><span class="sxs-lookup"><span data-stu-id="eac56-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="eac56-113">Para mantener la compatibilidad con versiones de Windows Media Player Mobile anteriores a Windows Media Player 10 Mobile, el uso de "Marquis" en un archivo de definición de máscara todavía se considera válido.</span><span class="sxs-lookup"><span data-stu-id="eac56-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="eac56-114">Para obtener más información sobre la sección marquesina, vea [marquesina](marquee.md) en la referencia de máscara.</span><span class="sxs-lookup"><span data-stu-id="eac56-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eac56-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eac56-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac56-116">**Escritura del código**</span><span class="sxs-lookup"><span data-stu-id="eac56-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




