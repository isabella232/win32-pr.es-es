---
title: Instalación de descomprimores y descompresión
description: Instalación de descomprimores y descompresión
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Administrador de compresión de vídeo (VCM), instalación de instalaciones
- VCM (administrador de compresión de vídeo), instalación de instalaciones
- Función ICInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27a9bacc946a17bf4d70260cb077a7e3f17fe85760837cc7086144297f1f86c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140541"
---
# <a name="installing-compressors-and-decompressors"></a>Instalación de descomprimores y descompresión

En el ejemplo siguiente se muestra cómo una aplicación puede instalar una función como un descomprimidor o un descomprimidor mediante [**la función ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall)


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




