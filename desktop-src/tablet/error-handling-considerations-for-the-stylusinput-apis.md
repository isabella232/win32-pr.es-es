---
description: Información general sobre el control de errores al usar las interfaces de programación de aplicaciones (API) StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Consideraciones sobre el control de errores para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5056be9c9682eac66dbbec2a950794af27aa3e5282ad4bbc1539e042123ae5f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110935"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Consideraciones sobre el control de errores para StylusInput API

El objeto [**RealTimeStylus**](realtimestylus-class.md) detecta las excepciones no controladas producidas por un complemento. Cuando un complemento produce una excepción, se interrumpe el flujo normal de datos. El **objeto RealTimeStylus:**

1.  Crea un [objeto ErrorData](/previous-versions/ms575221(v=vs.100)) (en código administrado).
2.  Llama al método [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (en código administrado, el método [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.Error)](/previous-versions/ms824771(v=msdn.10)) del complemento que produjo la excepción.
3.  Llama al [**método Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) de los complementos restantes de esa colección.
4.  Si el complemento que produjo la excepción es un complemento sincrónico, el objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) (en código administrado) se agrega a la cola de salida.
5.  El [**objeto RealTimeStylus**](realtimestylus-class.md) reanuda el procesamiento normal de los datos originales.

Si un complemento produce una excepción desde su método [**Error,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) el objeto [**RealTimeStylus**](realtimestylus-class.md) detecta la excepción pero no genera un [nuevo objeto ErrorData.](/previous-versions/ms575221(v=vs.100)) Para obtener más información sobre cómo se agrega ErrorData a la cola, vea Datos de complemento y [la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

El [**objeto RealTimeStylus**](realtimestylus-class.md) no detiene el procesamiento de datos del flujo de datos del lápiz de tableta cuando uno de sus complementos produce una excepción. En función del diseño, es posible que algunos de los complementos deban suscribirse a la notificación [ErrorData](/previous-versions/ms575221(v=vs.100)) y modificar su comportamiento cuando se produce una excepción.

 

 
