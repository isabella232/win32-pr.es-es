---
description: La propiedad ProductLanguage se debe actualizar al identificador de idioma numérico (LANGID) del nuevo lenguaje.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Actualización de las propiedades ProductLanguage y ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678397"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Actualización de las propiedades ProductLanguage y ProductCode

La propiedad [**ProductLanguage**](productlanguage.md) se debe actualizar al identificador de idioma numérico (LANGID) del nuevo lenguaje. En el caso del ejemplo de localización, el valor de la propiedad **ProductLanguage** debe cambiarse del langid para inglés (1033) al langid para francés (1036) en la tabla de [propiedades](property-table.md).

El valor de la propiedad [**ProductCode**](productcode.md) en la [tabla de propiedades](property-table.md) debe cambiarse a un nuevo valor único al localizar una base de datos porque un producto localizado se considera un producto diferente. Por ejemplo, las versiones en alemán y en Inglés de una aplicación se consideran dos productos diferentes y deben tener distintos códigos de producto. Consulte [códigos de producto](product-codes.md).

Utilice el editor de tablas de base de datos para actualizar los valores de las propiedades ProductCode y ProductLanguage en la tabla de propiedades. No reutilice el GUID que se muestra si copia este ejemplo.

[Tabla de propiedades](property-table.md)



| Propiedad                                   | Value                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continuar](updating-a-summary-information-stream.md)

 

 



