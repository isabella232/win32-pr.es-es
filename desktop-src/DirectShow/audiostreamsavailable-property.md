---
description: La propiedad AudioStreamsAvailable recupera el número de secuencias de audio disponibles en el título actual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propiedad AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906548"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="53fd8-103">Propiedad AudioStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="53fd8-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="53fd8-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53fd8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="53fd8-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="53fd8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="53fd8-106">La `AudioStreamsAvailable` propiedad recupera el número de secuencias de audio disponibles en el título actual.</span><span class="sxs-lookup"><span data-stu-id="53fd8-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="53fd8-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53fd8-107">Return Value</span></span>

<span data-ttu-id="53fd8-108">Devuelve un valor entero comprendido entre 1 y 8 que representa el número de secuencias de audio disponibles en el título actual.</span><span class="sxs-lookup"><span data-stu-id="53fd8-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="53fd8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53fd8-109">Remarks</span></span>

<span data-ttu-id="53fd8-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="53fd8-110">This property is read-only with no default value.</span></span> <span data-ttu-id="53fd8-111">El uso principal de varias secuencias de audio es proporcionar bandas sonoras de películas en más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="53fd8-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="53fd8-112">Normalmente, no todos los títulos de un disco tienen habilitadas todas las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="53fd8-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="53fd8-113">Por ejemplo, la película de características podría tener bandas sonoras en tres idiomas diferentes, pero los finalizadores podrían tener solo una banda de reproducción en inglés.</span><span class="sxs-lookup"><span data-stu-id="53fd8-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="53fd8-114">Para que un usuario pueda seleccionar un flujo, la aplicación debe determinar qué secuencias están disponibles en el título actual.</span><span class="sxs-lookup"><span data-stu-id="53fd8-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="53fd8-115">Tenga en cuenta que los flujos concretos se identifican mediante un índice de cero a 7.</span><span class="sxs-lookup"><span data-stu-id="53fd8-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="53fd8-116">Normalmente, los discos presentan un menú que muestra las bandas sonoras disponibles, lo que permite al usuario seleccionar la secuencia de audio que se va a habilitar.</span><span class="sxs-lookup"><span data-stu-id="53fd8-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="53fd8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="53fd8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fd8-118">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="53fd8-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



