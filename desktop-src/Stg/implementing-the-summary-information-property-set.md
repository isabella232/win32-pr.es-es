---
title: Implementar el conjunto de propiedades de información de Resumen
description: Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para el almacenamiento estructurado.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementar el conjunto de propiedades de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772835"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementar el conjunto de propiedades de información de Resumen

Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para el almacenamiento estructurado.

A continuación se indican las instrucciones para implementar [el conjunto de propiedades de información de Resumen](the-summary-information-property-set.md):

-   **PID \_ de La plantilla** hace referencia a un documento externo que contiene información de formato y estilo. El proceso por el que se encuentra la plantilla está definido por la implementación.
-   **PID \_ de LASTAUTHOR** es el nombre almacenado en la información del usuario por la aplicación. Por ejemplo, Mary crea un documento en su equipo y lo asigna a John, que luego lo modifica y lo guarda. Mary es el autor, Juan es el último valor guardado por.
-   **PID \_ de REVNUMBER** es el número de veces que se ha llamado al comando File/Save en este documento.
-   Cada uno de los valores de fecha y hora debe almacenarse en la hora universal coordinada (UTC).
-   **PID \_ de CREATE \_ DTM** es una propiedad de solo lectura; Esta propiedad debe establecerse cuando se crea un documento, pero no debe cambiarse posteriormente.
-   En **la \_ miniatura de PID**, las aplicaciones deben almacenar datos en formato **CF \_ DIB** o **CF \_ METAFILEPICT** . **CF \_** Se recomienda METAFILEPICT.
-   **PID \_ de La seguridad** es el nivel de seguridad sugerido para el documento. Al anotar el nivel de seguridad del documento, una aplicación que no sea el autor del documento puede ajustar su interfaz de usuario a las propiedades. Una aplicación no debe mostrar ninguna información sobre un documento protegido mediante contraseña ni permitir modificaciones en los documentos Read-Only o bloqueados para anotaciones. Si el usuario intenta modificar propiedades, la aplicación debería advertir al usuario sobre el estado recomendado Read-Only.



| Nivel de seguridad         | Value |
|------------------------|-------|
| None                   | 0     |
| Contraseña protegida     | 1     |
| Recomendado solo lectura  | 2     |
| Solo lectura forzada     | 4     |
| Bloqueado para anotaciones | 8     |



 

 

 




