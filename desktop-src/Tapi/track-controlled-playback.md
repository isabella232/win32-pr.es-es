---
description: Los pasos siguientes se realizan para la reproducción controlada por seguimiento.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Track-Controlled reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687697"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="bdba4-103">Track-Controlled reproducción</span><span class="sxs-lookup"><span data-stu-id="bdba4-103">Track-Controlled Playback</span></span>

<span data-ttu-id="bdba4-104">Para realizar la reproducción controlada por seguimiento, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bdba4-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="bdba4-105">Seleccione el seguimiento de terminales en secuencias.</span><span class="sxs-lookup"><span data-stu-id="bdba4-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="bdba4-106">Cree el terminal de reproducción del archivo.</span><span class="sxs-lookup"><span data-stu-id="bdba4-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="bdba4-107">Establecer propiedades: el nombre de archivo y el tipo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="bdba4-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="bdba4-108">El uso de un método en el terminal de reproducción de archivos enumera los terminales de seguimiento de archivos.</span><span class="sxs-lookup"><span data-stu-id="bdba4-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="bdba4-109">Enumerar secuencias en la llamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="bdba4-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="bdba4-110">Seleccione el terminal de seguimiento de archivo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="bdba4-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="bdba4-111">Llame al método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el terminal de reproducción de archivos para iniciar la reproducción de datos grabados en las secuencias de TAPI.</span><span class="sxs-lookup"><span data-stu-id="bdba4-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 



