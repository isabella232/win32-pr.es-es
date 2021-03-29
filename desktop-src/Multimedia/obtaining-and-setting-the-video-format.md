---
title: Obtener y establecer el formato de vídeo
description: Obtener y establecer el formato de vídeo
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- capGetVideoFormat (macro)
- capGetVideoFormatSize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904587"
---
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="46daf-105">Obtener y establecer el formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="46daf-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="46daf-106">La estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) es de longitud variable para acomodar formatos de datos estándar y comprimidos.</span><span class="sxs-lookup"><span data-stu-id="46daf-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="46daf-107">Dado que esta estructura es de longitud variable, las aplicaciones siempre deben consultar el tamaño de la estructura y asignar memoria antes de recuperar el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="46daf-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="46daf-108">En el ejemplo siguiente se usa la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) para recuperar el tamaño del búfer y, a continuación, se llama a la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) para recuperar el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="46daf-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="46daf-109">Las aplicaciones pueden usar la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (o el mensaje de [**\_ \_ \_ videoformat Set Cap set de WM**](wm-cap-set-videoformat.md) ) para enviar una estructura de encabezado [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) a la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="46daf-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="46daf-110">Dado que los formatos de vídeo son específicos del dispositivo, la aplicación debe comprobar el valor devuelto para determinar si se aceptó el formato.</span><span class="sxs-lookup"><span data-stu-id="46daf-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46daf-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46daf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46daf-112">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="46daf-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 