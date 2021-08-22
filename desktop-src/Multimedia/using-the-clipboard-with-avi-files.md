---
title: Uso del Portapapeles con archivos AVI
description: Uso del Portapapeles con archivos AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Función AVIPutFileOnClipboard
- Función AVIGetFromClipboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579f7eeed3b5b7397e248bb1c9090bc086cb715c591ec436af5de7d885551c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687845"
---
# <a name="using-the-clipboard-with-avi-files"></a>Uso del Portapapeles con archivos AVI

El Portapapeles proporciona almacenamiento cómodo y temporal que una aplicación puede usar para copiar o transferir archivos AVI. AVIFile incluye funciones del Portapapeles que puede usar con archivos de disco o memoria.

Puede copiar un archivo en el Portapapeles mediante la [**función AVIPutFileOnClipboard.**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) Para escribir un archivo que se encuentra en el Portapapeles en la memoria o el disco, use la [**función AVIGetFromClipboard.**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)

Puede borrar un archivo del Portapapeles mediante la [**función AVIClearClipboard.**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) Esta función no borra otros tipos de información, como texto, del Portapapeles. Si usa funciones del Portapapeles en la aplicación, borre el Portapapeles con **AVIClearClipboard** antes de cerrar la aplicación o cerrar el archivo en el Portapapeles. Puede llamar a **AVIClearClipboard en** la aplicación independientemente de si se ha usado o no **AVIPutFileOnClipboard.**

> [!Note]  
> Si la aplicación copia un archivo en el Portapapeles y el archivo contiene datos de secuencia que pueden cambiar, puede crear un archivo de memoria de secuencias clonadas mediante la [**función AVIMakeFileFromStreams.**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) A continuación, puede colocar el archivo en el Portapapeles y, a continuación, liberar el archivo original sin invalidarlo.

 

 

 




