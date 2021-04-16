---
description: Futuras mejoras en el ejemplo de código de aplicación Winsock.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Mejoras futuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705617"
---
# <a name="future-improvements"></a>Mejoras futuras

Hay varias mejoras que se pueden realizar en esta aplicación, por ejemplo:

-   La aplicación puede crear una única conexión persistente. Tendría que agregarse el control de errores adecuado. Esto reduciría la sobrecarga asociada con el inicio y el desmontaje de la conexión.
-   El código de respuesta del servidor se puede optimizar para consolidar las respuestas, lo que reduce el número de paquetes enviados desde el servidor.
-   Se pueden realizar mejoras en el protocolo. Por ejemplo, se puede usar una máscara de máscara de actualización para indicar las celdas que se van a actualizar y solo los datos de las celdas que se envían.
-   Las actualizaciones pueden superponerse mediante diferentes subprocesos, de modo que la red no esté inactiva mientras la función **ComputeNext** se esté ejecutando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[La versión de línea base: una aplicación con un rendimiento muy deficiente](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisión 1: limpieza del manifiesto](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisión 2: rediseño para menos conexiones](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisión 3: envío de bloque comprimido](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



