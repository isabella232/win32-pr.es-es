---
description: Los terminales de archivo se pueden usar de dos maneras.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Uso de terminales de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156772"
---
# <a name="using-file-terminals"></a><span data-ttu-id="d39b6-103">Uso de terminales de archivo</span><span class="sxs-lookup"><span data-stu-id="d39b6-103">Using File Terminals</span></span>

<span data-ttu-id="d39b6-104">Los terminales de archivo se pueden usar de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="d39b6-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="d39b6-105">El método más sencillo consiste en usar [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) para seleccionar un terminal de archivo (reproducción o registro) en un objeto de llamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="d39b6-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="d39b6-106">En este caso, TAPI se encarga de conectar los flujos de audio a los terminales de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d39b6-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="d39b6-107">El segundo método permite que una aplicación tenga un mayor control sobre la asignación de secuencias de audio a las pistas.</span><span class="sxs-lookup"><span data-stu-id="d39b6-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="d39b6-108">En este escenario, la aplicación enumera las secuencias disponibles en la llamada, selecciona las que desea grabar (o utilizar para la reproducción), crea (o busca para la reproducción) las pistas correspondientes en el terminal de archivos y selecciona las pistas de las secuencias de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d39b6-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="d39b6-109">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d39b6-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d39b6-110">Reproducción simple</span><span class="sxs-lookup"><span data-stu-id="d39b6-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="d39b6-111">Reproducción controlada por seguimiento</span><span class="sxs-lookup"><span data-stu-id="d39b6-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="d39b6-112">Registro simple</span><span class="sxs-lookup"><span data-stu-id="d39b6-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="d39b6-113">Registro controlado por seguimiento</span><span class="sxs-lookup"><span data-stu-id="d39b6-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



