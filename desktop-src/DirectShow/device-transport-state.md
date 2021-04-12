---
description: Estado de transporte del dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Estado de transporte del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423163"
---
# <a name="device-transport-state"></a><span data-ttu-id="7ac90-103">Estado de transporte del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7ac90-103">Device Transport State</span></span>

<span data-ttu-id="7ac90-104">Para recuperar el estado actual del dispositivo, como reproducir, pausar o detener, llame al método [**IAMExtTransport:: get \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) .</span><span class="sxs-lookup"><span data-stu-id="7ac90-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="7ac90-105">El método recupera una constante que indica el estado del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7ac90-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="7ac90-106">Value</span><span class="sxs-lookup"><span data-stu-id="7ac90-106">Value</span></span>                    | <span data-ttu-id="7ac90-107">Estado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7ac90-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="7ac90-108">\_reproducción en modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="7ac90-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="7ac90-109">Reproducir</span><span class="sxs-lookup"><span data-stu-id="7ac90-109">Play</span></span>         |
| <span data-ttu-id="7ac90-110">\_detención del modo de Ed \_</span><span class="sxs-lookup"><span data-stu-id="7ac90-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="7ac90-111">Stop</span><span class="sxs-lookup"><span data-stu-id="7ac90-111">Stop</span></span>         |
| <span data-ttu-id="7ac90-112">modo de ED \_ \_ congelar</span><span class="sxs-lookup"><span data-stu-id="7ac90-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="7ac90-113">Pausar</span><span class="sxs-lookup"><span data-stu-id="7ac90-113">Pause</span></span>        |
| <span data-ttu-id="7ac90-114">\_modo Ed \_ FF</span><span class="sxs-lookup"><span data-stu-id="7ac90-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="7ac90-115">Avance rápido</span><span class="sxs-lookup"><span data-stu-id="7ac90-115">Fast-forward</span></span> |
| <span data-ttu-id="7ac90-116">\_modo Ed \_ Rebo</span><span class="sxs-lookup"><span data-stu-id="7ac90-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="7ac90-117">Rebobinar</span><span class="sxs-lookup"><span data-stu-id="7ac90-117">Rewind</span></span>       |
| <span data-ttu-id="7ac90-118">\_registro en modo Ed \_</span><span class="sxs-lookup"><span data-stu-id="7ac90-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="7ac90-119">Registro</span><span class="sxs-lookup"><span data-stu-id="7ac90-119">Record</span></span>       |
| <span data-ttu-id="7ac90-120">inmovilización de registros en \_ modo Ed \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ac90-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="7ac90-121">Grabar-pausar</span><span class="sxs-lookup"><span data-stu-id="7ac90-121">Record-pause</span></span> |



 

<span data-ttu-id="7ac90-122">El código siguiente comprueba el estado del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7ac90-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="7ac90-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ac90-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac90-124">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="7ac90-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



