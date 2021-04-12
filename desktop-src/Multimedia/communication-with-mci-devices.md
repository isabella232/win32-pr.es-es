---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicarse
- MCIWndGetDeviceID (macro)
- mciSendCommand función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358832"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="b3432-106">Comunicación con dispositivos MCI</span><span class="sxs-lookup"><span data-stu-id="b3432-106">Communication with MCI Devices</span></span>

<span data-ttu-id="b3432-107">Es posible que cada dispositivo MCI utilice uno o varios de los siguientes identificadores:</span><span class="sxs-lookup"><span data-stu-id="b3432-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="b3432-108">un identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b3432-108">a device identifier</span></span>
-   <span data-ttu-id="b3432-109">un nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b3432-109">a device name</span></span>
-   <span data-ttu-id="b3432-110">un alias</span><span class="sxs-lookup"><span data-stu-id="b3432-110">an alias</span></span>
-   <span data-ttu-id="b3432-111">nombre de archivo del contenido cargado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b3432-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="b3432-112">MCIWnd proporciona macros que puede usar para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="b3432-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="b3432-113">Después, puede usar esta información para comunicarse a través de MCI directamente con dispositivos MCI asociados a MCIWnd Windows.</span><span class="sxs-lookup"><span data-stu-id="b3432-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="b3432-114">Puede recuperar el identificador del dispositivo MCI actual mediante la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="b3432-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="b3432-115">El identificador de dispositivo MCI es un valor numérico que identifica la instancia del dispositivo MCI que está usando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3432-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="b3432-116">La aplicación puede usar este identificador al comunicarse con un dispositivo MCI mediante la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3432-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="b3432-117">Para recuperar el nombre del dispositivo MCI actual, use la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="b3432-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="b3432-118">El nombre del dispositivo MCI es una cadena terminada en null que identifica el tipo de dispositivo asociado a una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b3432-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="b3432-119">La aplicación puede usar este nombre al comunicarse con un dispositivo MCI mediante **mciSendCommand**.</span><span class="sxs-lookup"><span data-stu-id="b3432-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="b3432-120">Puede recuperar el alias del dispositivo MCI actual mediante la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="b3432-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="b3432-121">La aplicación puede usar este alias al comunicarse con un dispositivo MCI mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3432-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="b3432-122">Por último, puede recuperar el nombre de archivo usado por un dispositivo MCI mediante la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="b3432-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="b3432-123">El nombre de archivo identifica el contenido asociado actualmente a una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b3432-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="b3432-124">La aplicación puede usar este nombre de archivo al comunicarse con un dispositivo MCI mediante **mciSendCommand** o **mciSendString**.</span><span class="sxs-lookup"><span data-stu-id="b3432-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 