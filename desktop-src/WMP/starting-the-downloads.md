---
title: Iniciar las descargas
description: Iniciar las descargas
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, iniciar descargas
- tiendas en línea, iniciar descargas
- tipo 2 tiendas en línea, iniciar descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- iniciar descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419085"
---
# <a name="starting-the-downloads"></a>Iniciar las descargas

La descarga se inicia cuando el usuario hace clic en **Descargar**. Este botón se denomina btnDownload en el código y la función de controlador de eventos para el evento **onclick** se denomina "aldescargar".

"Undownload" crea primero un nuevo objeto **DownloadCollection** vacío y lo asigna a una variable local.


```C++
oDLC = g_oManager.createDownloadCollection();

```



A continuación, la función inicia cada uno de los cinco elementos que se descargan y almacena el objeto **DownloadItem** devuelto en una matriz.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



A continuación, el código actualiza los elementos de la interfaz de usuario con la información sobre la colección de descarga y sus elementos de descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




