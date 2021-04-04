---
description: En este tema se proporciona un procedimiento para realizar grabaciones controladas por seguimiento de secuencias de audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910306"
---
# <a name="track-controlled-record"></a><span data-ttu-id="2bdf1-103">Track-Controlled registro</span><span class="sxs-lookup"><span data-stu-id="2bdf1-103">Track-Controlled Record</span></span>

<span data-ttu-id="2bdf1-104">En este tema se proporciona un procedimiento para realizar grabaciones controladas por seguimiento de secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="2bdf1-105">**Para realizar grabaciones controladas por seguimiento de secuencias de audio**</span><span class="sxs-lookup"><span data-stu-id="2bdf1-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="2bdf1-106">Seleccione Archivo seguimiento de terminales en secuencias.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="2bdf1-107">Cree el terminal del registro de archivos.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="2bdf1-108">Establezca el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-108">Set the file name.</span></span>
4.  <span data-ttu-id="2bdf1-109">Enumerar secuencias en la llamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="2bdf1-110">Para estos pasos, consulte el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="2bdf1-111">Llame al método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el terminal del registro de archivos para iniciar la grabación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="2bdf1-112">**Para enumerar secuencias en la llamada TAPI**</span><span class="sxs-lookup"><span data-stu-id="2bdf1-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="2bdf1-113">Cree una pista del mismo tipo de audio y dirección que la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="2bdf1-114">Establezca las propiedades de seguimiento para el formato de audio.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-114">Set the track properties for audio format.</span></span> <span data-ttu-id="2bdf1-115">Si no se establece, el formato será el mismo que el formato de las secuencias.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="2bdf1-116">Seleccione la pista en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-116">Select the track on the stream.</span></span>

<span data-ttu-id="2bdf1-117">Si se selecciona una pista en varios flujos, esto implica mezclar flujos.</span><span class="sxs-lookup"><span data-stu-id="2bdf1-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



