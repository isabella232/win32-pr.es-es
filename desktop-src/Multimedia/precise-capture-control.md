---
title: Control de captura preciso
description: Control de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funciones de devolución de llamada AVICap, control de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532085"
---
# <a name="precise-capture-control"></a>Control de captura preciso

Una ventana de captura puede proporcionar la función de devolución de llamada del control de captura con un control preciso sobre los momentos en que comienza y finaliza la captura de streaming. El primer mensaje enviado desde el controlador de captura al procedimiento de devolución de llamada establece el parámetro *nState* en CONTROLCALLBACK \_ preroll después de asignar todos los búferes y se completan todos los demás preparados de captura. Este mensaje ofrece a la aplicación la posibilidad de revertir los orígenes de vídeo. (La función de devolución de llamada especifica *nState* como el segundo parámetro). A continuación, la función de devolución de llamada devuelve en el momento en que se inicia la grabación exacta. Un valor devuelto de **true** desde la función de devolución de llamada continúa la captura. Un valor devuelto de **false** anula la captura. Una vez que se inicia la captura, se llama a la función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK \_ para permitir que la aplicación finalice la captura devolviendo **false**.

 

 




