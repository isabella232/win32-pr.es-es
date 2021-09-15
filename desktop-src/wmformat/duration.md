---
title: Duration
description: El atributo Duration contiene la duración de reproducción del archivo, en unidades de 100 nanosegundos.
ms.assetid: 1d72f826-4087-45f5-a5b9-f31c4e98e9b1
keywords:
- Formato multimedia de windows de duración
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ea9763bf505394f231ebe7d50943f4336e244c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360593"
---
# <a name="duration"></a>Duration

El **atributo Duration** contiene la duración de reproducción del archivo, en unidades de 100 nanosegundos.

## <a name="global-constant"></a>Constante global

g \_ wszWMDuration

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ QWORD**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




