---
description: Declare una clase de C++ que herede la clase base que eligió como parte de la escritura de un filtro de transformación.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Paso 2. Declarar la clase Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3e814802a67185f320345dea2f397188999ecafb9596b9b368a4b6eff8e240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652201"
---
# <a name="step-2-declare-the-filter-class"></a>Paso 2. Declarar la clase Filter

Este es el paso 2 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

Comience declarando una clase de C++ que hereda la clase base:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Cada una de las clases de filtro tiene clases de pin asociadas. En función de las necesidades específicas del filtro, es posible que tenga que invalidar las clases de pin. En el caso de **CTransformFilter,** los pines delegan la mayor parte de su trabajo en el filtro, por lo que probablemente no necesite invalidar los pines.

Debe generar un CLSID único para el filtro. Puede usar la utilidad Guidgen o Uuidgen; nunca copie un GUID existente. Hay varias maneras de declarar un CLSID. En el ejemplo siguiente se usa la macro **\_ DEFINE GUID:**


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



A continuación, escriba un método de constructor para el filtro:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Observe que uno de los parámetros del constructor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) es el CLSID definido anteriormente.

Siguiente: [Paso 3. Admitir negociación de tipos de medios](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



