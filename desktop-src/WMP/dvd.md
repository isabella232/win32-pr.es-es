---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrar DVDs
- Modelo de objetos de Windows Media Player, DVDs
- modelo de objetos, DVDs
- Control ActiveX de Windows Media Player, DVDs
- Control ActiveX, DVDs
- Control ActiveX móvil de Windows Media Player, DVDs
- Windows Media Player Mobile, migrar DVDs
- Guía de migración, DVDs
- Migración de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777161"
---
# <a name="dvd"></a><span data-ttu-id="a94d8-112">DVD</span><span class="sxs-lookup"><span data-stu-id="a94d8-112">DVD</span></span>

<span data-ttu-id="a94d8-113">El control ActiveX de Windows Media Player 6,4 contiene un objeto de **DVD** que expone diversos métodos y propiedades, así como un evento, para tratar específicamente con el contenido del DVD.</span><span class="sxs-lookup"><span data-stu-id="a94d8-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="a94d8-114">Por ejemplo, para determinar el número de títulos de DVD disponibles, se usa **Player6**. propiedad **titlesAvailable** :</span><span class="sxs-lookup"><span data-stu-id="a94d8-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="a94d8-115">El modelo de objetos de Windows Media Player 7 o posterior implementa un enfoque más integrado en DVD.</span><span class="sxs-lookup"><span data-stu-id="a94d8-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="a94d8-116">Las propiedades, los métodos y los eventos específicos de DVD solo se implementan si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a94d8-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="a94d8-117">De lo contrario, la funcionalidad del modelo de objetos existente funciona con los medios de DVD como cabría esperar.</span><span class="sxs-lookup"><span data-stu-id="a94d8-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="a94d8-118">Por ejemplo, para determinar el número de títulos de DVD disponibles cuando se usa Windows Media Player 7 o posterior, se recupera un objeto de **lista de reproducción** del objeto **CDROM** :</span><span class="sxs-lookup"><span data-stu-id="a94d8-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="a94d8-119">En el ejemplo anterior se recupera un objeto de **lista de reproducción** con una primera entrada que representa el DVD de la primera unidad.</span><span class="sxs-lookup"><span data-stu-id="a94d8-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="a94d8-120">Las entradas adicionales representan títulos de DVD individuales.</span><span class="sxs-lookup"><span data-stu-id="a94d8-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="a94d8-121">Por lo tanto, el número de títulos disponibles se puede calcular de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="a94d8-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="a94d8-122">Estas son las principales diferencias a tener en cuenta al migrar desde la versión 6,4:</span><span class="sxs-lookup"><span data-stu-id="a94d8-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="a94d8-123">La reproducción de DVD solo se admite cuando se usa Windows Media Player para Windows XP o posterior y el sistema operativo Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="a94d8-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="a94d8-124">Las unidades de DVD-ROM se enumeran exactamente igual que las unidades de CD-ROM mediante el objeto **CdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="a94d8-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="a94d8-125">Las unidades de DVD-ROM individuales se administran mediante el objeto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="a94d8-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="a94d8-126">El objeto **DVD** extiende el modelo de objetos con métodos y una propiedad específicamente para trabajar con DVD.</span><span class="sxs-lookup"><span data-stu-id="a94d8-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="a94d8-127">Hay dos nuevos eventos, **OpenPlaylistSwitch** y **DomainChange**, específicamente para trabajar con DVD.</span><span class="sxs-lookup"><span data-stu-id="a94d8-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="a94d8-128">El contenido del DVD se organiza mediante objetos de **lista de reproducción** y objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="a94d8-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="a94d8-129">Los idiomas de DVD se administran mediante la funcionalidad de lenguaje disponible en el objeto **Controls** (Windows Media Player 9 series o posterior).</span><span class="sxs-lookup"><span data-stu-id="a94d8-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="a94d8-130">Los controles de transporte y la información de posición para DVD funcionan igual que para otros tipos de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="a94d8-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a94d8-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a94d8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94d8-132">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="a94d8-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="a94d8-133">**Usar el control Media Player de Windows con Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="a94d8-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




