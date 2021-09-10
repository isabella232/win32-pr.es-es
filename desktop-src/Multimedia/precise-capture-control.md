---
title: Control de captura preciso
description: Control de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funciones de devolución de llamada AVICap, control de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372458"
---
# <a name="precise-capture-control"></a>Control de captura preciso

Una ventana de captura puede proporcionar a la función de devolución de llamada capture-control un control preciso sobre los momentos en que comienza y finaliza la captura de streaming. El primer mensaje enviado desde el controlador de captura al procedimiento de devolución de llamada establece el parámetro *nState* en CONTROLCALLBACK PREROLL después de asignar todos los búferes y todas las demás preparaciones de captura \_ se han completado. Este mensaje ofrece a la aplicación la capacidad de preinselección de los orígenes de vídeo. (La función de devolución de llamada *especifica nState* como su segundo parámetro). A continuación, la función de devolución de llamada devuelve en el momento exacto en que se va a iniciar la grabación. Un valor devuelto de **TRUE de** la función de devolución de llamada continúa la captura. Un valor devuelto de **FALSE** anula la captura. Una vez que comienza la captura, se llama a la función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK CAPTURING para permitir que la aplicación finalice la captura \_ devolviendo **FALSE**.

 

 




