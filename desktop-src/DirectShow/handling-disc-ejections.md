---
description: Control de expulsaciones de disco
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Control de expulsaciones de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906308"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="f13fe-103">Control de expulsaciones de disco</span><span class="sxs-lookup"><span data-stu-id="f13fe-103">Handling Disc Ejections</span></span>

<span data-ttu-id="f13fe-104">Cuando el usuario expulsa un DVD de la unidad, el explorador de DVD envía a la aplicación un \_ mensaje de extracción de disco DVD de EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f13fe-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="f13fe-105">La aplicación puede omitir este mensaje sin ningún riesgo y dejar que el navegador de DVD administre el estado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="f13fe-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="f13fe-106">Una aplicación también puede controlar el \_ \_ \_ método expulsado del disco DVD de EC para implementar el comportamiento personalizado cuando se expulsa un disco.</span><span class="sxs-lookup"><span data-stu-id="f13fe-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="f13fe-107">Si controla el mensaje, debe establecer la \_ marca ResetOnStop de DVD en **true** con el método [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y, a continuación, llamar a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) antes de cerrar la aplicación o reproducir otro disco.</span><span class="sxs-lookup"><span data-stu-id="f13fe-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f13fe-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f13fe-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13fe-109">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="f13fe-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



