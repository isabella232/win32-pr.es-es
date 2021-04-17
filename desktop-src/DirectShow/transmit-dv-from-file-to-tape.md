---
description: Transmisión de DV desde un archivo a una cinta
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmisión de DV desde un archivo a una cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668278"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="b3003-103">Transmisión de DV desde un archivo a una cinta</span><span class="sxs-lookup"><span data-stu-id="b3003-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="b3003-104">La transmisión desde un archivo AVI DV a una cinta VTR es complicada en cierto modo por el hecho de que los archivos pueden escribir-1 o el tipo 2.</span><span class="sxs-lookup"><span data-stu-id="b3003-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="b3003-105">Para transmitir un archivo DV a una cinta, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b3003-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="b3003-106">Cree una instancia del filtro del [controlador MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="b3003-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="b3003-107">Para obtener más información, consulte [seleccionar un dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="b3003-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="b3003-108">Asegúrese de que el dispositivo está en modo VTR.</span><span class="sxs-lookup"><span data-stu-id="b3003-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="b3003-109">De lo contrario, no puede transmitir a cinta. Vea [modo de dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b3003-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="b3003-110">Inicialice el generador de gráficos de captura, tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="b3003-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="b3003-111">Cree el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b3003-111">Build the graph.</span></span> <span data-ttu-id="b3003-112">La configuración del gráfico depende del tipo de archivo DV:</span><span class="sxs-lookup"><span data-stu-id="b3003-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="b3003-113">Transmisión del archivo de tipo 1</span><span class="sxs-lookup"><span data-stu-id="b3003-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="b3003-114">Transmisión desde el archivo de tipo 2</span><span class="sxs-lookup"><span data-stu-id="b3003-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="b3003-115">Ponga el dispositivo en modo de pausa de grabación, como se describe en [controlar una videocámara DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="b3003-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="b3003-116">PAUSE el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b3003-116">Pause the filter graph.</span></span> <span data-ttu-id="b3003-117">Mientras el gráfico de filtro está en pausa, envía un flujo continuo que repite el primer fotograma del vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3003-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="b3003-118">Para iniciar la transmisión, ponga el dispositivo en modo de registro y, a continuación, ejecute el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="b3003-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="b3003-119">Tarda en el dispositivo una cantidad de tiempo determinada hasta que el encabezado de grabación pueda grabarse, por lo que debe esperar unos dos segundos antes de ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b3003-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="b3003-120">Esto podría dar lugar a algunos fotogramas duplicados al principio de la cinta, pero garantiza que no se pierdan datos.</span><span class="sxs-lookup"><span data-stu-id="b3003-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3003-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3003-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3003-122">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3003-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



