---
title: Identificadores de formato
description: Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ec9e9843b1dfe843e89ebf85eadbbcb5da8cb58dfc1b289eb88c844aae7456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663155"
---
# <a name="format-identifiers"></a>Identificadores de formato

Los valores del conjunto de propiedades se almacenan en una sección etiquetada con un FMTID único. Por ejemplo, el FMTID del conjunto de propiedades Información de resumen COM **es F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Para definir un FMTID para el conjunto de propiedades Información de resumen, use la macro **DEFINE \_ GUID** en un archivo de include para el código que manipula el conjunto de propiedades.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Cualquier código que requiera FMTID para el conjunto de propiedades Información de resumen puede acceder a él a través de la variable *FMTID \_ SummaryInformation.*

Al almacenar conjuntos de propiedades [**en instancias de IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) convierta FMTID en un nombre de cadena para el objeto de almacenamiento.

 

 




