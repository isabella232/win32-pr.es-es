---
title: Control de captura preciso
description: Control de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funciones de devolución de llamada AVICap, control de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365482f5f6309f9642aa5c8b497b58a1d9416e398e5c3624191d777e006b23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372666"
---
# <a name="precise-capture-control"></a>Control de captura preciso

Una ventana de captura puede proporcionar a la función de devolución de llamada capture-control un control preciso sobre los momentos en que comienza y termina la captura de streaming. El primer mensaje enviado desde el controlador de captura al procedimiento de devolución de llamada establece el parámetro *nState* en CONTROLCALLBACK PREROLL después de asignar todos los búferes y se completan todos los demás preparativos de \_ captura. Este mensaje ofrece a la aplicación la capacidad de realizar la inscripción previa de los orígenes de vídeo. (La función de devolución de llamada *especifica nState* como su segundo parámetro). A continuación, la función de devolución de llamada devuelve en el momento exacto en que se va a iniciar la grabación. Un valor devuelto de **TRUE de la** función de devolución de llamada continúa la captura. Un valor devuelto de **false** anula la captura. Una vez que comienza la captura, se llama a la función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK CAPTURING para permitir que la aplicación finalice la captura \_ devolviendo **FALSE**.

 

 




