---
description: Control de tasa
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Control de tasa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715504"
---
# <a name="rate-control"></a><span data-ttu-id="42bfe-103">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="42bfe-103">Rate Control</span></span>

<span data-ttu-id="42bfe-104">La [sesión multimedia](media-session.md) permite cambiar la velocidad de reproducción, que puede usar una aplicación para implementar características de reproducción como el avance rápido y el rebobinado.</span><span class="sxs-lookup"><span data-stu-id="42bfe-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="42bfe-105">En esta sección se describe cómo las aplicaciones pueden cambiar la velocidad de reproducción mientras se usa la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="42bfe-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="42bfe-106">Para obtener información sobre cómo admitir el control de tasas en sus propios componentes de canalización, vea [implementar el control de tasa](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="42bfe-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="42bfe-107">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="42bfe-107">This section contains the following topics.</span></span>



| <span data-ttu-id="42bfe-108">Tema</span><span class="sxs-lookup"><span data-stu-id="42bfe-108">Topic</span></span>                                                                                                      | <span data-ttu-id="42bfe-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="42bfe-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="42bfe-110">Acerca del control tasa</span><span class="sxs-lookup"><span data-stu-id="42bfe-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="42bfe-111">Proporciona información general sobre el control de tasa.</span><span class="sxs-lookup"><span data-stu-id="42bfe-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="42bfe-112">Cómo determinar las tarifas admitidas</span><span class="sxs-lookup"><span data-stu-id="42bfe-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="42bfe-113">Cómo buscar las velocidades de reproducción más rápidas y más lentas admitidas.</span><span class="sxs-lookup"><span data-stu-id="42bfe-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="42bfe-114">Cómo establecer la velocidad de reproducción en la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="42bfe-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="42bfe-115">Cómo cambiar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="42bfe-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="42bfe-116">Cómo realizar la limpieza</span><span class="sxs-lookup"><span data-stu-id="42bfe-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="42bfe-117">Cómo desplazarse por un fotograma de vídeo a la vez.</span><span class="sxs-lookup"><span data-stu-id="42bfe-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="42bfe-118">Control de tasa de implementación</span><span class="sxs-lookup"><span data-stu-id="42bfe-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="42bfe-119">Cómo admitir las tasas de reproducción de variables en un componente de canalización personalizado.</span><span class="sxs-lookup"><span data-stu-id="42bfe-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="42bfe-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42bfe-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42bfe-121">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="42bfe-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="42bfe-122">Búsqueda, avance rápido y reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="42bfe-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



