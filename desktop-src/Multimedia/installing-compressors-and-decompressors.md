---
title: Instalación de decompresores y descompresión
description: Instalación de decompresores y descompresión
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Administrador de compresión de vídeo (VCM), instalación de los programas
- VCM (administrador de compresión de vídeo), instalación de paquetes
- Función ICInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370400"
---
# <a name="installing-compressors-and-decompressors"></a>Instalación de decompresores y descompresión

En el ejemplo siguiente se muestra cómo una aplicación puede instalar una función como un descompresión o un descompresión mediante [**la función ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall)


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




