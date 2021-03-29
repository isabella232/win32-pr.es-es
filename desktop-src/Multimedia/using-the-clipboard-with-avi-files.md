---
title: Usar el Portapapeles con archivos AVI
description: Usar el Portapapeles con archivos AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard función)
- AVIGetFromClipboard función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776158"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="45182-105">Usar el Portapapeles con archivos AVI</span><span class="sxs-lookup"><span data-stu-id="45182-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="45182-106">El portapapeles proporciona un almacenamiento temporal y práctico que una aplicación puede usar para copiar o transferir archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="45182-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="45182-107">AVIFile incluye funciones del portapapeles que puede usar con archivos de disco o de memoria.</span><span class="sxs-lookup"><span data-stu-id="45182-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="45182-108">Puede copiar un archivo en el portapapeles mediante la función [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) .</span><span class="sxs-lookup"><span data-stu-id="45182-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="45182-109">Para escribir un archivo que se encuentra en el portapapeles en la memoria o en el disco, use la función [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .</span><span class="sxs-lookup"><span data-stu-id="45182-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="45182-110">Puede borrar un archivo del portapapeles mediante la función [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) .</span><span class="sxs-lookup"><span data-stu-id="45182-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="45182-111">Esta función no borra otros tipos de información, como texto, del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="45182-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="45182-112">Si usa funciones del portapapeles en la aplicación, borre el Portapapeles con **AVIClearClipboard** antes de cerrar la aplicación o cierre el archivo en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="45182-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="45182-113">Puede llamar a **AVIClearClipboard** en su aplicación tanto si se ha usado **AVIPutFileOnClipboard** como si no.</span><span class="sxs-lookup"><span data-stu-id="45182-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="45182-114">Si la aplicación copia un archivo en el portapapeles y el archivo contiene datos de secuencia que pueden cambiar, puede crear un archivo de memoria de secuencias clonadas mediante la función [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="45182-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="45182-115">Después, puede colocar el archivo en el portapapeles y, a continuación, liberar el archivo original sin invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="45182-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




