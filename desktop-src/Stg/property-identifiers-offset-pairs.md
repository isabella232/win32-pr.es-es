---
title: Identificadores de propiedad/pares de desplazamiento
description: El valor del conjunto de propiedades Recuento de propiedades es una matriz de valores de conjunto de propiedades Identificadores de propiedad/Pares de desplazamiento.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50d69d4027e1513ee099be79d9ef8819c71f6e31ba5aad173cbfe4778e6d9d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960771"
---
# <a name="property-identifiersoffset-pairs"></a>Identificadores de propiedad/pares de desplazamiento

El valor del conjunto de propiedades Recuento de propiedades es una matriz de valores de conjunto de propiedades Identificadores de propiedad/Pares de desplazamiento. Los identificadores de propiedad son valores de 32 bits que identifican de forma única una propiedad dentro de una sección. Los pares de desplazamiento indican la distancia desde el inicio de la sección hasta el inicio de la propiedad Type/Value Pair. Dado que los desplazamientos son relativos a la sección, las secciones se pueden copiar como una matriz de bytes.

Los identificadores de propiedad no se ordenan en ningún orden determinado. Las propiedades se pueden omitir del conjunto de propiedades almacenadas; los lectores no deben basarse en un orden o intervalo específico de identificadores de propiedad.

 

 




