---
description: Establecer la velocidad de reproducción
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Establecer la velocidad de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686266"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="436bb-103">Establecer la velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="436bb-103">Setting the Playback Rate</span></span>

<span data-ttu-id="436bb-104">Para cambiar la velocidad de reproducción, llame al método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="436bb-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="436bb-105">Especifique la nueva tasa como una fracción de la tasa original.</span><span class="sxs-lookup"><span data-stu-id="436bb-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="436bb-106">Por ejemplo, para reproducir dos veces la velocidad normal, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="436bb-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="436bb-107">Las velocidades mayores que uno son más rápidas que las normales.</span><span class="sxs-lookup"><span data-stu-id="436bb-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="436bb-108">Las velocidades entre cero y uno son más lentas que las normales.</span><span class="sxs-lookup"><span data-stu-id="436bb-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="436bb-109">Las tasas negativas se definen como reproducción hacia atrás, pero en la práctica la mayoría de los filtros no la admiten.</span><span class="sxs-lookup"><span data-stu-id="436bb-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="436bb-110">Actualmente ninguno de los filtros de DirectShow estándar admite la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="436bb-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="436bb-111">Independientemente de la velocidad de reproducción, la posición actual y la posición de detención siempre se expresan en relación con el origen original.</span><span class="sxs-lookup"><span data-stu-id="436bb-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="436bb-112">Por ejemplo, si un archivo de origen tiene una duración de 20 segundos a una velocidad de reproducción normal, al establecer la posición actual en 10 segundos, se buscará en el medio del archivo.</span><span class="sxs-lookup"><span data-stu-id="436bb-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="436bb-113">Si la velocidad de reproducción es 2,0, la posición de detención es de 20 segundos y se busca en la posición de 10 segundos, el archivo se reproducirá durante 5 segundos de tiempo real: 10 segundos, como mínimo, la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="436bb-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="436bb-114">En una velocidad de reproducción de 2,0, la posición actual aumenta al doble de la velocidad del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="436bb-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



