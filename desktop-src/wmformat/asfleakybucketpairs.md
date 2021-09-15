---
title: ASFLeakyBucketPairs
description: El atributo ASFLeakyBucketPairs es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs windows Media Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359938"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

El **atributo ASFLeakyBucketPairs** es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.

## <a name="global-constant"></a>Constante global

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo de datos

**BINARIO DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Este atributo tiene el formato siguiente:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Donde *wReserved debe* ser igual a cero y *bucket* es una matriz de estructuras [**WM \_ LEAKY BUCKET \_ \_ PAIR.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) La matriz debe contener al menos dos entradas, pero puede ser mayor. El objeto reader usa este atributo para determinar la cantidad de contenido que se va a almacenar en búfer antes de la reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




