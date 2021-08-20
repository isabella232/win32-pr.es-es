---
description: Script de ASF Secuencias en DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Script de ASF Secuencias en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdb83746fed5022ce5050cef0e615e57619c8b5394ae0f57ce0b979a1fb5bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001465"
---
# <a name="asf-script-streams-in-directshow"></a>Script de ASF Secuencias en DirectShow

Cuando se le da un archivo que incluye un flujo de tipo script WMMEDIATYPE al filtro lector [DE ASF](wm-asf-reader-filter.md) de WM, crea una marca de salida para él que se puede conectar al filtro Representador de comandos de \_ script interno. [](internal-script-command-renderer-filter.md) Cuando se llama [**a IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ese filtro se agrega automáticamente al gráfico y se conecta. Cuando el representador de comandos de script interno recibe un ejemplo que contiene un comando de script, se produce un evento [**\_ OLE \_ EVENT**](ec-ole-event.md) de EC cuyo *lParam* contiene el script. La aplicación es totalmente responsable de controlar este evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



