---
description: Paso 2.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Paso 2. Declarar la clase de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678219"
---
# <a name="step-2-declare-the-filter-class"></a>Paso 2. Declarar la clase de filtro

Este es el paso 2 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

Empiece por declarar una clase de C++ que herede la clase base:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Cada una de las clases de filtro tiene asociadas clases de PIN. En función de las necesidades específicas del filtro, puede que tenga que invalidar las clases de PIN. En el caso de **CTransformFilter**, los pin delegan la mayor parte del trabajo en el filtro, por lo que probablemente no sea necesario invalidar los pin.

Debe generar un CLSID único para el filtro. Puede usar la utilidad Guidgen o uuidgen; no copie nunca un GUID existente. Hay varias maneras de declarar un CLSID. En el ejemplo siguiente se usa la macro **definir \_ GUID** :


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



Tenga en cuenta que uno de los parámetros para el constructor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) es el CLSID definido anteriormente.

Siguiente: [paso 3. Compatibilidad con la negociación de tipos de medios](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



