---
title: Iniciar las descargas
description: Iniciar las descargas
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media en línea, iniciar descargas
- tiendas en línea, iniciar descargas
- tiendas en línea de tipo 2, iniciar descargas
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- inicio de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995075"
---
# <a name="starting-the-downloads"></a>Iniciar las descargas

La descarga se inicia cuando el usuario hace clic en **Descargar**. Este botón se denomina btnDownload en el código y la función de controlador de eventos para el evento **onClick** se denomina "OnDownload".

"OnDownload" crea primero un nuevo objeto **DownloadCollection** vacío y lo asigna a una variable local.


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

[**Uso del Administrador de descargas**](using-the-download-manager.md)
</dt> </dl>

 

 




