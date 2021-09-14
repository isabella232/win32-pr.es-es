---
description: En Monitor de red, la estructura CAPTUREFILTER define el filtro de captura.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Estructura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245120"
---
# <a name="the-capturefilter-structure"></a>Estructura CAPTUREFILTER

En Monitor de red, la [estructura](capture-filters.md) [**CAPTUREFILTER**](capturefilter.md) define el filtro de captura. La ausencia o combinación de marcas, valores y expresiones determina qué marcos se pasarán o se van a eliminar por el controlador Monitor de red datos. En la ilustración siguiente se muestran las tres áreas del análisis del filtro de captura: Etype/SAP, address y pattern match.

![tres áreas del análisis del filtro de captura](images/capfilter.png)

En la tabla siguiente se muestra la función de cada elemento de filtro de captura.



| Filter, elemento                                       | Acción                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etype/SAP](writing-etypesap-filter-portion.md)     | Evalúa la configuración de Etype/SAP. La combinación de marcas determina qué tipos o valores de configuración se incluyen o excluyen.                                                                                    |
| [Dirección](writing-addresstable-filter-portion.md)   | Evalúa las direcciones de origen y destino y los pares de direcciones. Las distintas combinaciones de marcas determinan qué valores individuales o combinaciones de pares de direcciones se incluyen o excluyen.                   |
| [Coincidencia de patrones](writing-the-patternmatch-filter.md) | Define coincidencias de patrones complejos dentro de un marco. Se proporcionan marcas para distintos tipos y desplazamientos. Puede combinar coincidencias de patrón con instrucciones de operador AND u OR lógicas.                              |
| [Recorte](clipping-a-frame.md)                     | Recorta los fotogramas de una manera especificada por varios valores de bytes. Solo puede usar este elemento para recortar todos los fotogramas o usarlo con otros elementos de filtro de captura. por ejemplo, para buscar y, a continuación, recortar un solo fotograma. |
| [**Detonante**](trigger.md)                           | Este elemento de filtro de captura está obsoleto. Los desencadenadores ya no forman parte de un filtro de captura; ahora están contenidos en sus propias etiquetas BLOB, que se especifican por separado.                                     |



 

Un fotograma se evalúa con respecto a las tres partes del filtro de captura. Por lo tanto, un marco transmitido correctamente debe pasar cada elemento. Tenga en cuenta que Monitor de red controlador evalúa la ausencia de cualquiera de los tres elementos como **TRUE.** Por ejemplo, el controlador evalúa la ausencia de una sección Etype/SAP como "TODOS los fotogramas con el valor ANY Etype/SAP son válidos".

 

 



