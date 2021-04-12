---
title: Secuencias de comandos en DirectShow
description: Secuencias de comandos en DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- DirectShow, secuencias de scripts
- secuencias de scripts, DirectShow
- secuencias, secuencias de scripts en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357646"
---
# <a name="script-streams-in-directshow"></a>Secuencias de comandos en DirectShow

Cuando se proporciona al filtro de lector ASF de WM un archivo que incluye una secuencia de tipo WMMEDIATYPE \_ script, se crea un PIN de salida para él que se puede conectar al filtro de representador de comandos de script interno de DirectShow. Cuando se llama a **IGraphBuilder:: RenderFile**, ese filtro se agrega automáticamente al gráfico y se conecta. Cuando el representador del comando de script interno recibe un ejemplo que contiene un comando de script, desencadena un **\_ \_ evento OLE de EC** cuyo **lParam** contiene el script. La aplicación es totalmente responsable de controlar este evento. Para obtener más información sobre el **\_ \_ evento OLE de EC**, vea la documentación del SDK de DirectShow.

 

 




