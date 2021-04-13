---
title: Elegir archivos
description: Elegir archivos
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- crear máscaras, elegir archivos
- Aspectos de Windows Media Player, elegir archivos
- máscaras, elegir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269221"
---
# <a name="choosing-files"></a><span data-ttu-id="65cac-106">Elegir archivos</span><span class="sxs-lookup"><span data-stu-id="65cac-106">Choosing Files</span></span>

<span data-ttu-id="65cac-107">Si desea elegir un archivo, puede usar código similar al ejemplo de lista de reproducción, pero sustituya lo siguiente por la sección PLAYELEMENT:</span><span class="sxs-lookup"><span data-stu-id="65cac-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="65cac-108">Esta línea usará el método **openDialog** de **Theme** para definir una **dirección URL** para el reproductor.</span><span class="sxs-lookup"><span data-stu-id="65cac-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="65cac-109">Puede utilizar esta opción para elegir archivos que no están en listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="65cac-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="65cac-110">Puede ver un ejemplo de **openDialog** en funcionamiento similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="65cac-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65cac-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65cac-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65cac-112">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="65cac-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




