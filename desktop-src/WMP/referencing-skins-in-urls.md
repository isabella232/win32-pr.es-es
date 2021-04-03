---
title: Referencia a máscaras en direcciones URL
description: Referencia a máscaras en direcciones URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Máscaras de Windows Media Player, referencias de URL
- máscaras, referencias de URL
- Referencias a direcciones URL en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779584"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="79066-106">Referencia a máscaras en direcciones URL</span><span class="sxs-lookup"><span data-stu-id="79066-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="79066-107">Si usa una dirección URL para cargar un archivo multimedia que reproducirá Windows Media Player, puede solicitar que se use una máscara determinada con ese archivo.</span><span class="sxs-lookup"><span data-stu-id="79066-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="79066-108">Si la máscara ya está instalada en el equipo del usuario, se utilizará; de lo contrario, se usará la máscara anterior.</span><span class="sxs-lookup"><span data-stu-id="79066-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="79066-109">Para solicitar una máscara, agregue lo siguiente al final de la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="79066-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="79066-110">*skinName* es el nombre de la máscara que desea solicitar.</span><span class="sxs-lookup"><span data-stu-id="79066-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="79066-111">No use comillas alrededor del nombre de la máscara.</span><span class="sxs-lookup"><span data-stu-id="79066-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="79066-112">Por ejemplo, para solicitar que se use la máscara headspace, escriba la siguiente dirección URL http:</span><span class="sxs-lookup"><span data-stu-id="79066-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="79066-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79066-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79066-114">**Acerca de las máscaras**</span><span class="sxs-lookup"><span data-stu-id="79066-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




