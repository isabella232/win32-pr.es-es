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
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="e83db-106">Configuración de compresores y descompresores</span><span class="sxs-lookup"><span data-stu-id="e83db-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="e83db-107">En el ejemplo siguiente se usa la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para mostrar cómo se comprueba si un compresor es compatible con el cuadro de diálogo de configuración y para mostrarlo en caso de que lo tenga.</span><span class="sxs-lookup"><span data-stu-id="e83db-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="e83db-108">En el ejemplo siguiente se muestra cómo obtener los datos de estado mediante la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="e83db-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="e83db-109">En el ejemplo siguiente se muestra cómo restaurar los datos de estado mediante la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="e83db-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="e83db-110">Los datos de estado restaurados por las aplicaciones no deben contener ningún cambio en los datos de estado obtenidos de un controlador.</span><span class="sxs-lookup"><span data-stu-id="e83db-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




