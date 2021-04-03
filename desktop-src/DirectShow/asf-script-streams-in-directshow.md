---
description: Secuencias de script ASF en DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Secuencias de script ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997941"
---
# <a name="asf-script-streams-in-directshow"></a>Secuencias de script ASF en DirectShow

Cuando se proporciona al filtro de [lector ASF de WM](wm-asf-reader-filter.md) un archivo que incluye una secuencia de tipo WMMEDIATYPE \_ script, se crea un PIN de salida para él que se puede conectar al filtro de [representador del comando de script interno](internal-script-command-renderer-filter.md) . Cuando se llama a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ese filtro se agrega automáticamente al gráfico y se conecta. Cuando el representador del comando de script interno recibe un ejemplo que contiene un comando de script, activa un evento de [**\_ \_ evento OLE de EC**](ec-ole-event.md) cuyo *lParam* contiene el script. La aplicación es totalmente responsable de controlar este evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



