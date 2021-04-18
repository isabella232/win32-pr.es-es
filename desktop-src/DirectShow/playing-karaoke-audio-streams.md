---
description: Reproducir flujos de audio de karaoke
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Reproducir flujos de audio de karaoke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677146"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="ee316-103">Reproducir flujos de audio de karaoke</span><span class="sxs-lookup"><span data-stu-id="ee316-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="ee316-104">El navegador de DVD puede reproducir discos DVD-Video con secuencias de audio de karaoke, pero la reproducción de karaoke también requiere un descodificador que admita la combinación de Karaoke de multicanal.</span><span class="sxs-lookup"><span data-stu-id="ee316-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="ee316-105">En concreto, el descodificador debe admitir el [**conjunto de propiedades de Karaoke de DVD**](dvd-karaoke-property-set.md) ( \_ propiedad \_ DVDKARAOKE).</span><span class="sxs-lookup"><span data-stu-id="ee316-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="ee316-106">Los discos de karaoke son un tipo de disco DVD-Video y tienen la misma estructura de navegación.</span><span class="sxs-lookup"><span data-stu-id="ee316-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="ee316-107">Las canciones suelen tener el formato de títulos y los títulos se pueden agrupar en conjuntos de títulos basados en el rendimiento, estilo musical u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="ee316-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="ee316-108">La diferencia principal entre el karaoke y otros tipos de DVD-Videos es la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="ee316-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="ee316-109">Los discos de karaoke contienen audio multicanal, normalmente Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="ee316-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="ee316-110">Los canales 0 y 1 siempre contienen la música instrumental de fondo, mientras que los canales del 2 al 5 pueden contener cualquier combinación de voces guía, Melodies de guía y efectos sonoros.</span><span class="sxs-lookup"><span data-stu-id="ee316-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="ee316-111">Una aplicación de Karaoke puede controlar el volumen y el altavoz de destino para cada canal auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ee316-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="ee316-112">Cuando el navegador de DVD detecta el contenido de karaoke en un disco y entra en el modo de karaoke, informa al descodificador, que debe silenciar los tres canales superiores (los canales auxiliares) hasta que una aplicación Active explícitamente cualquiera de ellos.</span><span class="sxs-lookup"><span data-stu-id="ee316-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="ee316-113">Las tareas básicas de una aplicación de karaoke son:</span><span class="sxs-lookup"><span data-stu-id="ee316-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="ee316-114">Determine el número de canales auxiliares y su contenido mediante métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .</span><span class="sxs-lookup"><span data-stu-id="ee316-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="ee316-115">Proporcione una interfaz de usuario que muestre el contenido del canal y permita a los usuarios activar o desactivar cualquier canal auxiliar en cualquier momento, mediante [**IDvdControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span><span class="sxs-lookup"><span data-stu-id="ee316-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="ee316-116">Estos pasos se ilustran en la aplicación de ejemplo de DVD en DVDCore. cpp en el método **GetAudioAttributes** .</span><span class="sxs-lookup"><span data-stu-id="ee316-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee316-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee316-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee316-118">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="ee316-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



