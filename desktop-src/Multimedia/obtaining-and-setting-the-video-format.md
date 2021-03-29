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
# <a name="obtaining-and-setting-the-video-format"></a>Obtener y establecer el formato de vídeo

La estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) es de longitud variable para acomodar formatos de datos estándar y comprimidos. Dado que esta estructura es de longitud variable, las aplicaciones siempre deben consultar el tamaño de la estructura y asignar memoria antes de recuperar el formato de vídeo actual. En el ejemplo siguiente se usa la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) para recuperar el tamaño del búfer y, a continuación, se llama a la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) para recuperar el formato de vídeo actual.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Las aplicaciones pueden usar la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (o el mensaje de [**\_ \_ \_ videoformat Set Cap set de WM**](wm-cap-set-videoformat.md) ) para enviar una estructura de encabezado [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) a la ventana de captura. Dado que los formatos de vídeo son específicos del dispositivo, la aplicación debe comprobar el valor devuelto para determinar si se aceptó el formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 