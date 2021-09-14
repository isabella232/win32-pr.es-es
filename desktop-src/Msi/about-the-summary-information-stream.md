---
description: El flujo de información de resumen contiene información sobre el paquete que se puede ver a través de Microsoft Windows Explorer.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Acerca del flujo de información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159255"
---
# <a name="about-the-summary-information-stream"></a>Acerca del flujo de información de resumen

El flujo de información de resumen contiene información sobre el paquete que se puede ver a través de Microsoft Windows Explorer. Esta información es accesible a través de **la interfaz IStream.** Es el autor el que debe proporcionar los valores de cada una de estas propiedades.

El flujo de información de resumen usa COM para proporcionar almacenamiento estructurado de bases de datos. COM admite el concepto de almacenamiento estructurado accesible a través de la **interfaz IStream.** El almacenamiento estructurado, a su vez, admite el concepto de conjuntos de propiedades como un método flexible para serializar casi cualquier información. La especificación COM define un único conjunto de propiedades estándar, información de resumen, que se usa para rellenar hojas de propiedades que se pueden ver desde Windows Explorer. Por lo tanto, los usuarios pueden ver la información almacenada en el flujo de información de resumen cuando hacen clic con el botón derecho en una base de datos del instalador o se transforman y [seleccionan Propiedades.](about-properties.md)

Para obtener una lista del conjunto de propiedades de resumen, [vea Summary Information Stream Property Set](summary-information-stream-property-set.md).

Para obtener descripciones breves de las propiedades de información de resumen usadas con bases de datos, transformaciones y revisiones, vea Resumen de descripciones [de propiedades](summary-property-descriptions.md).

 

 



