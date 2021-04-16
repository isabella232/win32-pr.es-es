---
description: En el siguiente tema se describe cómo realizar una reproducción simple.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Reproducción simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678454"
---
# <a name="simple-playback"></a><span data-ttu-id="2e3c8-103">Reproducción simple</span><span class="sxs-lookup"><span data-stu-id="2e3c8-103">Simple Playback</span></span>

<span data-ttu-id="2e3c8-104">En el siguiente tema se describe cómo realizar una reproducción simple.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="2e3c8-105">**Para realizar una reproducción simple**</span><span class="sxs-lookup"><span data-stu-id="2e3c8-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="2e3c8-106">Seleccione el terminal de reproducción de archivos en el nivel de llamada.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="2e3c8-107">Cree el terminal de reproducción en la llamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="2e3c8-108">Establecer propiedades: el nombre de archivo y el tipo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="2e3c8-109">Llame al método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el terminal de reproducción de archivos para iniciar la reproducción de secuencias.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="2e3c8-110">En el código de ejemplo siguiente se muestra la reproducción simple.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="2e3c8-111">En primer lugar, use la interfaz [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) para crear el terminal para la grabación.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="2e3c8-112">Esto indica a TSP/MSP que realice la reproducción de archivos en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="2e3c8-113">El TSP/MSP crea un terminal para que lo use la aplicación y lo devuelve si se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="2e3c8-114">Obtiene el puntero de la interfaz [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) desde la interfaz de terminal y úselo para establecer el nombre de archivo que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="2e3c8-115">Suponiendo que el archivo contenga una secuencia de audio y que la llamada tenga una secuencia de audio de captura, el contenido de audio del archivo se reproducirá en esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="2e3c8-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



