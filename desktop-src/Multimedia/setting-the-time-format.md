---
title: Establecer el formato de hora
description: Establecer el formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904551"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="d0a3c-104">Establecer el formato de hora</span><span class="sxs-lookup"><span data-stu-id="d0a3c-104">Setting the Time Format</span></span>

<span data-ttu-id="d0a3c-105">Use el mensaje del comando [**\_ set de MCI**](mci-set.md) junto con la estructura de [**parms de MCI \_ set \_**](mci-set-parms.md) para establecer el formato de hora para un dispositivo abierto.</span><span class="sxs-lookup"><span data-stu-id="d0a3c-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="d0a3c-106">Establezca el miembro **dwTimeFormat** en una de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="d0a3c-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="d0a3c-107">Constante</span><span class="sxs-lookup"><span data-stu-id="d0a3c-107">Constant</span></span>                   | <span data-ttu-id="d0a3c-108">Formato de hora</span><span class="sxs-lookup"><span data-stu-id="d0a3c-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="d0a3c-109">\_bytes de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d0a3c-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="d0a3c-110">Bytes (en archivos con formato PCM modulado de código \[ \] )</span><span class="sxs-lookup"><span data-stu-id="d0a3c-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="d0a3c-111">formato MCI en \_ \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="d0a3c-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="d0a3c-112">Milisegundos</span><span class="sxs-lookup"><span data-stu-id="d0a3c-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="d0a3c-113">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="d0a3c-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="d0a3c-114">Minuto/segundo/marco</span><span class="sxs-lookup"><span data-stu-id="d0a3c-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="d0a3c-115">\_ejemplos de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d0a3c-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="d0a3c-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d0a3c-116">Samples</span></span>                                              |
| <span data-ttu-id="d0a3c-117">\_Formato MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="d0a3c-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="d0a3c-118">SMPTE, 24 fotogramas</span><span class="sxs-lookup"><span data-stu-id="d0a3c-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="d0a3c-119">\_Formato MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="d0a3c-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="d0a3c-120">SMPTE, 25 fotograma</span><span class="sxs-lookup"><span data-stu-id="d0a3c-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="d0a3c-121">\_Formato MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="d0a3c-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="d0a3c-122">SMPTE, 30 fotogramas</span><span class="sxs-lookup"><span data-stu-id="d0a3c-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="d0a3c-123">\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="d0a3c-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="d0a3c-124">SMPTE, 30 fotogramas de colocación</span><span class="sxs-lookup"><span data-stu-id="d0a3c-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="d0a3c-125">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="d0a3c-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="d0a3c-126">Pista/minuto/segundo/marco</span><span class="sxs-lookup"><span data-stu-id="d0a3c-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="d0a3c-127">\_ \_ formato \_ SONGPTR de MCI SEQ</span><span class="sxs-lookup"><span data-stu-id="d0a3c-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="d0a3c-128">Puntero de canción MIDI</span><span class="sxs-lookup"><span data-stu-id="d0a3c-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="d0a3c-129">En el ejemplo siguiente se establece el formato de hora en milisegundos en el dispositivo especificado por la variable wDeviceID con la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d0a3c-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 