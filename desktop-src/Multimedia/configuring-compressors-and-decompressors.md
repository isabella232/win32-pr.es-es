---
title: Configuración de descompresores y descompresión
description: Configuración de descompresores y descompresión
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Administrador de compresión de vídeo (VCM), configuración de vehículos
- VCM (administrador de compresión de vídeo), configuración de resaltes
- ICQueryConfigure macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144928"
---
# <a name="configuring-compressors-and-decompressors"></a>Configuración de descompresores y descompresión

En el ejemplo siguiente se usa la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para demostrar cómo probar si un elemento de apoyo admite el cuadro de diálogo de configuración y mostrarlo si lo hace.


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



 

 




