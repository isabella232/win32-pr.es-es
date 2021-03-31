---
title: Configuración de compresores y descompresores
description: Configuración de compresores y descompresores
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Administrador de compresión de vídeo (VCM), configurar compresores
- VCM (Administrador de compresión de vídeo), configurar compresores
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418625"
---
# <a name="configuring-compressors-and-decompressors"></a>Configuración de compresores y descompresores

En el ejemplo siguiente se usa la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para mostrar cómo se comprueba si un compresor es compatible con el cuadro de diálogo de configuración y para mostrarlo en caso de que lo tenga.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



En el ejemplo siguiente se muestra cómo obtener los datos de estado mediante la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



En el ejemplo siguiente se muestra cómo restaurar los datos de estado mediante la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) . Los datos de estado restaurados por las aplicaciones no deben contener ningún cambio en los datos de estado obtenidos de un controlador.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




