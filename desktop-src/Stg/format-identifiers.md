---
title: Identificadores de formato
description: Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356989"
---
# <a name="format-identifiers"></a>Identificadores de formato

Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único. Por ejemplo, FMTID para el conjunto de propiedades de información de Resumen de COM es **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Para definir un FMTID para el conjunto de propiedades de información de Resumen, use la macro **definir \_ GUID** en un archivo de inclusión para el código que manipula el conjunto de propiedades.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Cualquier código que requiera el valor de FMTID para el conjunto de propiedades de información de resumen puede acceder a él a través de la variable *\_ SummaryInformation de FMTID* .

Al almacenar conjuntos de propiedades en instancias de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , convierta FMTID en un nombre de cadena para el objeto de almacenamiento.

 

 




