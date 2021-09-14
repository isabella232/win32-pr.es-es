---
description: Asf Script Secuencias en DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Asf Script Secuencias en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162262"
---
# <a name="asf-script-streams-in-directshow"></a>Asf Script Secuencias en DirectShow

Cuando se le da al filtro [lector DE ASF](wm-asf-reader-filter.md) de WM un archivo que incluye una secuencia de tipo script WMMEDIATYPE, crea un pin de salida para él que se puede conectar al filtro Representador de comandos de \_ script interno. [](internal-script-command-renderer-filter.md) Cuando se llama [**a IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ese filtro se agrega automáticamente al gráfico y se conecta. Cuando el representador de comandos de script interno recibe un ejemplo que contiene un comando de script, se produce un evento [**\_ OLE \_ EVENT**](ec-ole-event.md) de EC cuyo *lParam* contiene el script. La aplicación es totalmente responsable de controlar este evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



