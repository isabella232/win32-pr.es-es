---
description: Mejoras futuras en el código de la aplicación Winsock de ejemplo.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Mejoras futuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068278"
---
# <a name="future-improvements"></a>Mejoras futuras

Hay varias mejoras que se pueden realizar en esta aplicación, como:

-   La aplicación podría crear una conexión única y persistente. Se tendría que agregar el control de errores adecuado. Esto reduciría la sobrecarga asociada con el inicio y la desmontaje de la conexión.
-   El código de respuesta del servidor podría optimizarse para consolidar las respuestas, lo que reduce el número de paquetes enviados desde el servidor.
-   Se podrían realizar mejoras en el protocolo. Por ejemplo, se podría usar una máscara de bits de actualización para indicar qué celdas se van a actualizar y solo los datos de celda enviados.
-   Las actualizaciones se podrían superponer mediante subprocesos diferentes, de modo que la red no esté inactiva mientras se **ejecuta la función ComputeNext.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[La versión de línea base: una aplicación con un rendimiento muy bajo](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisión 1: Limpiar lo obvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisión 2: Rediseño para menos conectos](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisión 3: Envío de bloque comprimido](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



