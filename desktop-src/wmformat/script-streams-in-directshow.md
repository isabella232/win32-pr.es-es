---
title: Script Secuencias en DirectShow
description: Script Secuencias en DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, secuencias de script
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), secuencias de script
- ASF (formato de sistemas avanzados), secuencias de script
- DirectShow,secuencias de script
- secuencias de script, DirectShow
- streams,script streams in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929626"
---
# <a name="script-streams-in-directshow"></a>Script Secuencias en DirectShow

Cuando se le da un archivo que incluye un flujo de tipo script WMMEDIATYPE al filtro lector DE ASF de WM, crea una marca de salida para él que se puede conectar al filtro representador de comandos de script interno de \_ DirectShow. Cuando se llama **a IGraphBuilder::RenderFile**, ese filtro se agrega automáticamente al gráfico y se conecta. Cuando el representador de comandos de script interno recibe un ejemplo que contiene un comando de script, se produce un evento **\_ OLE \_ DE EC** cuyo **lParam** contiene el script. La aplicación es totalmente responsable de controlar este evento. Para obtener más información sobre **EC \_ OLE \_ EVENT**, consulte la documentación DirectShow SDK.

 

 




