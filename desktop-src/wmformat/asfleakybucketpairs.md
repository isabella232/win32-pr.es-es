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
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434624"
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

 

 




