---
description: La secuencia de información de Resumen contiene información sobre el paquete que se puede ver a través del explorador de Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Acerca del flujo de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156356"
---
# <a name="about-the-summary-information-stream"></a>Acerca del flujo de información de Resumen

La secuencia de información de Resumen contiene información sobre el paquete que se puede ver a través del explorador de Microsoft Windows. Esta información es accesible a través de la interfaz **IStream** . Es el autor quien debe proporcionar los valores de cada una de estas propiedades.

La secuencia de información de Resumen utiliza COM para proporcionar almacenamiento estructurado de bases de datos. COM admite el concepto de almacenamiento estructurado accesible a través de la interfaz **IStream** . El almacenamiento estructurado, a su vez, admite el concepto de conjuntos de propiedades como un método flexible para serializar casi cualquier información. La especificación COM define un conjunto de propiedades estándar único, información de Resumen, que se usa para rellenar las hojas de propiedades visibles desde el explorador de Windows. Por lo tanto, los usuarios pueden ver la información almacenada en la secuencia de información de resumen al hacer clic con el botón secundario en una base de datos del instalador o en transformar y seleccionar [propiedades](about-properties.md).

Para obtener una lista del conjunto de propiedades de Resumen, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).

Para obtener breves descripciones de las propiedades de información de Resumen utilizadas con las bases de datos, las transformaciones y las revisiones, vea [descripciones de propiedades de Resumen](summary-property-descriptions.md).

 

 



