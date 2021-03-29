---
description: En Monitor de red, el filtro de captura se define mediante la estructura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Estructura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001225"
---
# <a name="the-capturefilter-structure"></a>Estructura CAPTUREFILTER

En Monitor de red, el [filtro de captura](capture-filters.md) se define mediante la estructura [**CAPTUREFILTER**](capturefilter.md) . La ausencia o combinación de marcas, valores y expresiones determina los fotogramas que el controlador Monitor de red pasará o quitará. En la ilustración siguiente se muestran las tres áreas del análisis del filtro de captura: ETYPE/SAP, dirección y coincidencia de patrones.

![tres áreas del análisis del filtro de captura](images/capfilter.png)

En la tabla siguiente se muestra la función de cada elemento de filtro de captura.



| Filter, elemento                                       | Acción                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ETYPE/SAP](writing-etypesap-filter-portion.md)     | Evalúa la configuración de ETYPE/SAP. La combinación de marcas determina qué tipos o valores de configuración se incluyen o excluyen.                                                                                    |
| [Dirección](writing-addresstable-filter-portion.md)   | Evalúa las direcciones de origen y de destino y los pares de direcciones. Diferentes combinaciones de marcas determinan qué valores individuales o combinaciones de pares de direcciones se incluyen o excluyen.                   |
| [Coincidencia de patrones](writing-the-patternmatch-filter.md) | Define coincidencias de patrones complejas dentro de un marco. Las marcas se proporcionan para distintos tipos y desplazamientos. Puede combinar las coincidencias de patrón con las instrucciones de operador AND u OR lógico.                              |
| [Recorte](clipping-a-frame.md)                     | Recorta los fotogramas de forma especificada por varios valores de byte. Solo puede usar este elemento para recortar todos los marcos o utilizarlos con otros elementos de filtro de captura; por ejemplo, para buscar y después recortar un solo fotograma. |
| [**Activado**](trigger.md)                           | Este elemento de filtro de captura está obsoleto. Los desencadenadores ya no forman parte de un filtro de captura; ahora están contenidas en sus propias etiquetas BLOB, que se especifican por separado.                                     |



 

Un marco se evalúa con las tres partes del filtro de captura. Por lo tanto, una trama transmitida correctamente debe pasar cada elemento. Tenga en cuenta que el controlador de Monitor de red evalúa la ausencia de cualquiera de los tres elementos como **true**. Por ejemplo, el controlador evalúa la ausencia de una sección ETYPE/SAP como "todos los marcos con el valor ETYPE/SAP son válidos".

 

 



