---
title: Control de captura preciso
description: Control de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funciones de devolución de llamada de AVICap, control de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169574"
---
# <a name="precise-capture-control"></a>Control de captura preciso

Una ventana de captura puede proporcionar a la función de devolución de llamada de control de captura un control preciso sobre los momentos en que comienza y termina la captura de streaming. El primer mensaje enviado desde el controlador de captura al procedimiento de devolución de llamada establece el parámetro *nState* en CONTROLCALLBACK PREROLL después de asignar todos los búferes y todas las demás preparaciones de captura \_ se han completado. Este mensaje ofrece a la aplicación la capacidad de realizar la inscripción previa de los orígenes de vídeo. (La función de devolución de llamada *especifica nState* como su segundo parámetro). A continuación, la función de devolución de llamada devuelve en el momento exacto en que se inicia la grabación. Un valor devuelto de **TRUE de la** función de devolución de llamada continúa la captura. Un valor devuelto de **FALSE** anula la captura. Una vez que comienza la captura, se llama a la función de devolución de llamada con frecuencia con *nState* establecido en CONTROLCALLBACK CAPTURING para permitir que la aplicación finalice la captura \_ devolviendo **FALSE**.

 

 




