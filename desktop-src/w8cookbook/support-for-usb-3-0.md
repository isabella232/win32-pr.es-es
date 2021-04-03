---
title: Compatibilidad con USB 3,0
description: Compatibilidad con USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794218"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="fdc4f-103">Compatibilidad con USB 3,0</span><span class="sxs-lookup"><span data-stu-id="fdc4f-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="fdc4f-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="fdc4f-104">Platforms</span></span>

<span data-ttu-id="fdc4f-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="fdc4f-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fdc4f-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdc4f-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fdc4f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdc4f-107">Description</span></span>

<span data-ttu-id="fdc4f-108">En Windows 8 y Windows Server 2012, se ha agregado compatibilidad con USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="fdc4f-109">Para ello, hemos agregado una nueva pila de software para potenciar el controlador de host USB 3,0, denominado controlador de host extensible (XHC).</span><span class="sxs-lookup"><span data-stu-id="fdc4f-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="fdc4f-110">Mantuvimos la paridad de la interfaz, el nivel de IRQL, el contexto del autor de la llamada, el estado de error, la frecuencia de reintento, etc.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="fdc4f-111">No debe haber ninguna diferencia cuando interactúe con un dispositivo conectado a través de USB 2,0 frente a USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="fdc4f-112">Sin embargo, si está escribiendo un controlador para un nuevo dispositivo USB 3,0, definitivamente opta por las nuevas capacidades de USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="fdc4f-113">Manifestación</span><span class="sxs-lookup"><span data-stu-id="fdc4f-113">Manifestation</span></span>

<span data-ttu-id="fdc4f-114">Las transferencias de dispositivos son más rápidas y el consumo de energía de un equipo de dispositivos USB es menor.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="fdc4f-115">Existe el riesgo de que los dispositivos USB existentes no funcionen correctamente cuando se conectan a un puerto USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="fdc4f-116">Esto no debería ocurrir y no se espera, pero, dado que el software que alimenta USB 3,0 es nuevo, es un riesgo.</span><span class="sxs-lookup"><span data-stu-id="fdc4f-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




