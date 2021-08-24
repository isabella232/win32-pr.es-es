---
title: Implementar el conjunto de propiedades de información de resumen
description: Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para structured Storage.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementar el conjunto de propiedades de información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe847d9a7353074727c94250d0f1ec1fec2194b5b7d250099464a86667861f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796915"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementar el conjunto de propiedades de información de resumen

Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para structured Storage.

Estas son las directrices para implementar [el conjunto de propiedades de información de resumen](the-summary-information-property-set.md):

-   **PID \_ TEMPLATE** hace referencia a un documento externo que contiene información de formato y estilo. El proceso por el que se encuentra la plantilla está definido por la implementación.
-   **PID \_ LASTAUTHOR es** el nombre almacenado en información de usuario por la aplicación. Por ejemplo, Mary crea un documento en su equipo y lo entrega a Juan, que luego lo modifica y lo guarda. Mary es la autora, Juan es la última guardada por valor.
-   **PID \_ REVNUMBER** es el número de veces que se ha llamado al comando File/Save en este documento.
-   Cada uno de los valores de fecha y hora debe almacenarse en hora universal coordinada (UTC).
-   **PID \_ CREATE \_ DTM** es una propiedad de solo lectura; Esta propiedad debe establecerse cuando se crea un documento, pero no se debe cambiar posteriormente.
-   Para **PID \_ THUMBNAIL,** las aplicaciones deben almacenar datos en formato **CF \_ DIB** o **CF \_ METAFILEPICT.** **CF \_ Se recomienda METAFILEPICT.**
-   **PID \_ SECURITY** es el nivel de seguridad sugerido para el documento. Al tener en cuenta el nivel de seguridad en el documento, una aplicación que no sea el originador del documento puede ajustar su interfaz de usuario a las propiedades. Una aplicación no debe mostrar ninguna información sobre un documento protegido con contraseña ni habilitar modificaciones en los documentos Read-Only o bloqueados para anotaciones. Si el usuario intenta modificar las propiedades, la aplicación debe advertir al usuario sobre el Read-Only recomendado.



| Nivel de seguridad         | Value |
|------------------------|-------|
| Ninguno                   | 0     |
| Protección con contraseña     | 1     |
| Se recomienda solo lectura  | 2     |
| Aplicación de solo lectura     | 4     |
| Bloqueado para anotaciones | 8     |



 

 

 




