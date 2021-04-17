---
title: ASFLeakyBucketPairs
description: El atributo ASFLeakyBucketPairs es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs formato de Windows Media
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695508"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

El atributo **ASFLeakyBucketPairs** es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.

## <a name="global-constant"></a>Constante global

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ binario**

## <a name="remarks"></a>Observaciones

Este atributo tiene el siguiente formato:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Donde *wReserved* debe ser igual a cero y *bucket* es una matriz de estructuras de pares de [**\_ \_ depósitos \_ con fugas de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) . La matriz debe contener al menos dos entradas, pero puede ser mayor. El objeto lector utiliza este atributo para determinar la cantidad de contenido que se va a almacenar en búfer antes de la reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




