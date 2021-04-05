---
description: Información general sobre el control de errores al usar las interfaces de programación de aplicaciones (API) de StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Consideraciones sobre el control de errores de la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001194"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Consideraciones sobre el control de errores de la API de StylusInput

El objeto [**RealTimeStylus**](realtimestylus-class.md) detecta las excepciones no controladas producidas por un complemento. Cuando un complemento inicia una excepción, se interrumpe el flujo de datos normal. El objeto **RealTimeStylus** :

1.  Crea un objeto [datoserror](/previous-versions/ms575221(v=vs.100)) (en código administrado).
2.  Llama al método [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (en el código administrado, el método [Microsoft. StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) ) del complemento que produjo la excepción.
3.  Llama al método [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) del resto de complementos de la colección.
4.  Si el complemento que inició la excepción es un complemento sincrónico, el objeto [datoserror](/previous-versions/ms575221(v=vs.100)) (en código administrado) se agrega a la cola de salida.
5.  El objeto [**RealTimeStylus**](realtimestylus-class.md) reanuda el procesamiento normal de los datos originales.

Si un complemento produce una excepción de su método de [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , el objeto [**RealTimeStylus**](realtimestylus-class.md) detecta la excepción pero no genera un nuevo objeto [datoserror](/previous-versions/ms575221(v=vs.100)) . Para obtener más información sobre cómo se agrega Datoserror a la cola, vea [los datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) no detiene el procesamiento de los datos del flujo de datos del lápiz de Tablet PC cuando uno de sus complementos produce una excepción. Dependiendo del diseño, algunos de los complementos pueden necesitar suscribirse a la notificación [datoserror](/previous-versions/ms575221(v=vs.100)) y modificar su comportamiento cuando se produce una excepción.

 

 
