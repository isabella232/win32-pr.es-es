---
description: El tipo de datos de hora de referencia \_ define las unidades de los tiempos de referencia en DirectShow. Cada unidad de tiempo de referencia es de 100 nanosegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690853"
---
# <a name="reference_time"></a>tiempo de referencia \_

El tipo de datos de **\_ hora de referencia** define las unidades de los tiempos de referencia en DirectShow. Cada unidad de tiempo de referencia es de 100 nanosegundos.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Observaciones

El tipo de datos de **\_ hora de referencia** es un entero de 64 bits.

Los tiempos de referencia se miden normalmente a partir de una de las siguientes líneas base:

-   Una hora de reloj absoluta. En este caso, la línea base dependerá de la implementación del reloj. Para obtener más información, consulte [relojes de referencia](reference-clocks.md).
-   Relativa al inicio de la reproducción.

Para obtener más información acerca de los tiempos de referencia, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Strmif. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos de DirectShow](directshow-data-types.md)
</dt> </dl>

 

 




