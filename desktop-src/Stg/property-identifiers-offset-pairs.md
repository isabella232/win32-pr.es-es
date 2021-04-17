---
title: Identificadores de propiedad/pares de desplazamiento
description: Después del recuento de propiedades, el valor del conjunto de propiedades es una matriz de valores del conjunto de propiedades de identificadores de propiedad/pares de desplazamiento.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665745"
---
# <a name="property-identifiersoffset-pairs"></a>Identificadores de propiedad/pares de desplazamiento

Después del recuento de propiedades, el valor del conjunto de propiedades es una matriz de valores del conjunto de propiedades de identificadores de propiedad/pares de desplazamiento. Los identificadores de propiedad son valores de 32 bits que identifican de forma única una propiedad dentro de una sección. Los pares de desplazamiento indican la distancia desde el inicio de la sección al inicio del par tipo-valor de propiedad. Dado que los desplazamientos son relativos a la sección, las secciones se pueden copiar como una matriz de bytes.

Los identificadores de propiedad no se ordenan en ningún orden determinado. Las propiedades se pueden omitir en el conjunto de propiedades almacenado. los lectores no deben basarse en un orden específico o en un intervalo de identificadores de propiedad.

 

 




