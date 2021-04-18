---
title: Comunicación con dispositivos MCI
description: Comunicación con dispositivos MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString (macro)
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651346"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="4e673-105">Comunicación con dispositivos MCI</span><span class="sxs-lookup"><span data-stu-id="4e673-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="4e673-106">El controlador de cada dispositivo MCI mantiene una lista de la configuración y las capacidades actuales, de modo que puede emitir una respuesta precisa cuando se consulta información.</span><span class="sxs-lookup"><span data-stu-id="4e673-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="4e673-107">Si desea comunicarse con un dispositivo MCI, puede usar las macros y funciones de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="4e673-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="4e673-108">Muchos de los comandos y consultas de MCI más comunes se definen como macros.</span><span class="sxs-lookup"><span data-stu-id="4e673-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="4e673-109">Sin embargo, si la tarea que desea realizar no está disponible como una función o macro, puede enviar comandos MCI directamente al controlador de dispositivo mediante la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o mediante el formulario de mensaje o la forma de cadena de los comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="4e673-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="4e673-110">El uso de la macro **MCIWndSendString** es equivalente a utilizar la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4e673-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="4e673-111">Los parámetros de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) solo incluyen el identificador de ventana y la forma de cadena del comando.</span><span class="sxs-lookup"><span data-stu-id="4e673-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="4e673-112">Para recuperar la información devuelta por un comando de cadena, use la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="4e673-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="4e673-113">Para obtener más información acerca de MCI, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="4e673-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="4e673-114">Debe excluir el alias del dispositivo del comando MCI al usar **MCIWndSendString**.</span><span class="sxs-lookup"><span data-stu-id="4e673-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="4e673-115">La biblioteca MCIWnd agrega este alias cuando envía el comando al dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4e673-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 