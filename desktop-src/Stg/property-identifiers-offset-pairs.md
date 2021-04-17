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
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="cdc5c-103">Identificadores de propiedad/pares de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="cdc5c-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="cdc5c-104">Después del recuento de propiedades, el valor del conjunto de propiedades es una matriz de valores del conjunto de propiedades de identificadores de propiedad/pares de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="cdc5c-105">Los identificadores de propiedad son valores de 32 bits que identifican de forma única una propiedad dentro de una sección.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="cdc5c-106">Los pares de desplazamiento indican la distancia desde el inicio de la sección al inicio del par tipo-valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="cdc5c-107">Dado que los desplazamientos son relativos a la sección, las secciones se pueden copiar como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="cdc5c-108">Los identificadores de propiedad no se ordenan en ningún orden determinado.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="cdc5c-109">Las propiedades se pueden omitir en el conjunto de propiedades almacenado. los lectores no deben basarse en un orden específico o en un intervalo de identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cdc5c-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




