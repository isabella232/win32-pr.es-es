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
# <a name="using-the-clipboard-with-avi-files"></a>Usar el Portapapeles con archivos AVI

El portapapeles proporciona un almacenamiento temporal y práctico que una aplicación puede usar para copiar o transferir archivos AVI. AVIFile incluye funciones del portapapeles que puede usar con archivos de disco o de memoria.

Puede copiar un archivo en el portapapeles mediante la función [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) . Para escribir un archivo que se encuentra en el portapapeles en la memoria o en el disco, use la función [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .

Puede borrar un archivo del portapapeles mediante la función [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) . Esta función no borra otros tipos de información, como texto, del portapapeles. Si usa funciones del portapapeles en la aplicación, borre el Portapapeles con **AVIClearClipboard** antes de cerrar la aplicación o cierre el archivo en el portapapeles. Puede llamar a **AVIClearClipboard** en su aplicación tanto si se ha usado **AVIPutFileOnClipboard** como si no.

> [!Note]  
> Si la aplicación copia un archivo en el portapapeles y el archivo contiene datos de secuencia que pueden cambiar, puede crear un archivo de memoria de secuencias clonadas mediante la función [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . Después, puede colocar el archivo en el portapapeles y, a continuación, liberar el archivo original sin invalidarlo.

 

 

 




