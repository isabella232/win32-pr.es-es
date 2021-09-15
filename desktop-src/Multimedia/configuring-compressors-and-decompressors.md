---
title: Configuración de descomprimores y descompresión
description: Configuración de descomprimores y descompresión
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Administrador de compresión de vídeo (VCM), configuración de ingerentes
- VCM (administrador de compresión de vídeo), configuración de ingerentes
- ICQueryConfigure macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476859"
---
# <a name="configuring-compressors-and-decompressors"></a>Configuración de descomprimores y descompresión

En el ejemplo siguiente se usa la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para mostrar cómo probar si un aseador admite el cuadro de diálogo de configuración y mostrarlo si lo hace.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



En el ejemplo siguiente se muestra cómo obtener los datos de estado mediante la macro [**ICGetState.**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



En el ejemplo siguiente se muestra cómo restaurar datos de estado mediante la macro [**ICSetState.**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) Los datos de estado restaurados por las aplicaciones no deben contener ningún cambio en los datos de estado obtenidos de un controlador.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




