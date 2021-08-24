---
description: La propiedad ProductLanguage debe actualizarse al identificador numérico de idioma (LANGID) del nuevo idioma.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Actualizar las propiedades ProductLanguage y ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d6cbb47a16e0e0f2f9d696dc73d3f3fe0d1bc278c4631a99469168e2ca23d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809865"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Actualizar las propiedades ProductLanguage y ProductCode

La [**propiedad ProductLanguage**](productlanguage.md) debe actualizarse al identificador numérico de idioma (LANGID) del nuevo idioma. En el caso del ejemplo de localización, el valor de la propiedad **ProductLanguage** debe cambiarse de LANGID para inglés (1033) a LANGID para francés (1036) en la tabla [Property](property-table.md).

El valor de la [**propiedad ProductCode**](productcode.md) de la tabla [Property](property-table.md) debe cambiarse a un nuevo valor único al localizar una base de datos porque un producto localizado se considera un producto diferente. Por ejemplo, las versiones en alemán e inglés de una aplicación se consideran dos productos diferentes y deben tener códigos de producto diferentes. Vea [Códigos de producto](product-codes.md).

Use el editor de tablas de base de datos para actualizar los valores de las propiedades ProductCode y ProductLanguage en la tabla Property. No reutilice el GUID que se muestra si copia este ejemplo.

[Tabla de propiedades](property-table.md)



| Propiedad                                   | Valor                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continuar](updating-a-summary-information-stream.md)

 

 



