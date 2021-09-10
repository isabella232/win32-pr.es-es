---
title: Captura de datos
description: Captura de datos
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- CapCaptureSequence macro
- capFileSaveAs macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371347"
---
# <a name="capturing-data"></a>Captura de datos

En el ejemplo siguiente se usa la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) para iniciar la captura de vídeo y la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) para copiar los datos capturados del archivo de captura en el archivo NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




