---
description: Cómo selecciona el navegador de DVD de Microsoft la región de DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Cómo selecciona el navegador de DVD de Microsoft la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677041"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="d156c-103">Cómo selecciona el navegador de DVD de Microsoft la región de DVD</span><span class="sxs-lookup"><span data-stu-id="d156c-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="d156c-104">El navegador de DVD de Microsoft usa el siguiente algoritmo para determinar la coincidencia de región mientras se reproducen discos DVD en un equipo:</span><span class="sxs-lookup"><span data-stu-id="d156c-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="d156c-105">El navegador de DVD obtiene la región del disco, la región de la unidad y la región del descodificador.</span><span class="sxs-lookup"><span data-stu-id="d156c-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="d156c-106">Si la región de disco es "todas las regiones", el navegador de DVD reproduce el disco.</span><span class="sxs-lookup"><span data-stu-id="d156c-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="d156c-107">Si el disco no está marcado para todas las regiones, el explorador de DVD comprueba si el descodificador tiene una región preestablecida.</span><span class="sxs-lookup"><span data-stu-id="d156c-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="d156c-108">Si el descodificador tiene una región preestablecida y no coincide con la región de disco, el navegador de DVD devuelve un error que indica que no puede reproducir el disco en la configuración actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="d156c-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="d156c-109">Abandonar</span><span class="sxs-lookup"><span data-stu-id="d156c-109">(Exit)</span></span>
5.  <span data-ttu-id="d156c-110">Si la región del descodificador no está establecida o es la misma que la región del disco, el explorador de DVD comprueba si la región de la unidad es la misma que la región de disco.</span><span class="sxs-lookup"><span data-stu-id="d156c-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="d156c-111">Si la región de unidad coincide con la región de disco, el explorador de DVD reproduce el título.</span><span class="sxs-lookup"><span data-stu-id="d156c-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="d156c-112">De lo contrario, si la región del controlador no coincide con la región del disco, el navegador de DVD invoca el código para cambiar la región de la unidad.</span><span class="sxs-lookup"><span data-stu-id="d156c-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="d156c-113">Si se ha agotado el número permitido de cambios en la región, se produce un error en el intento de cambio de región y no se puede reproducir el título en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="d156c-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d156c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d156c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d156c-115">Compatibilidad de cambio de región de DVD en Windows</span><span class="sxs-lookup"><span data-stu-id="d156c-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



