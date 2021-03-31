---
title: Grabación multimedia
description: Grabación multimedia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate función)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418669"
---
# <a name="multimedia-recording"></a><span data-ttu-id="6720f-105">Grabación multimedia</span><span class="sxs-lookup"><span data-stu-id="6720f-105">Multimedia Recording</span></span>

<span data-ttu-id="6720f-106">Puede implementar capacidades de grabación en la aplicación mediante la interfaz de usuario integrada en MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6720f-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="6720f-107">Puede usar la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para proporcionar controles para iniciar y detener la grabación y para guardar la información registrada.</span><span class="sxs-lookup"><span data-stu-id="6720f-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="6720f-108">Con **MCIWndCreate**, puede especificar estilos de ventana para mostrar una ventana de MCIWnd e incluir el botón **grabar** en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6720f-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="6720f-109">Con **MCIWndNew**, puede especificar el tipo de dispositivo que se va a grabar y especificar que la información se va a capturar en un archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="6720f-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="6720f-110">Si la aplicación requiere más sofisticación, puede automatizar y personalizar la grabación mediante la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="6720f-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="6720f-111">Para obtener más información, vea [personalizar el proceso de grabación](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="6720f-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="6720f-112">Algunos dispositivos, como el audio de CD y MCIAVI, se usan solo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6720f-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="6720f-113">Otros dispositivos, como los dispositivos de audio de forma de onda, se pueden usar para la grabación.</span><span class="sxs-lookup"><span data-stu-id="6720f-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="6720f-114">Si especifica un dispositivo que no puede grabar, MCIWnd omite el botón **grabar** de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6720f-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




