---
description: El tipo de datos REFERENCE \_ TIME define las unidades para los tiempos de referencia en DirectShow. Cada unidad de tiempo de referencia es de 100 nanosegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f1600e820ac59c53144743933701a61e4a7b753f814dde06c5c663a760938d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747325"
---
# <a name="reference_time"></a>TIEMPO DE \_ REFERENCIA

El **tipo de datos REFERENCE \_ TIME** define las unidades para los tiempos de referencia en DirectShow. Cada unidad de tiempo de referencia es de 100 nanosegundos.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Comentarios

El **tipo de datos REFERENCE \_ TIME** es un entero de 64 bits.

Normalmente, los tiempos de referencia se miden a partir de una de las líneas base siguientes:

-   Una hora de reloj absoluta. En este caso, la línea base dependerá de la implementación del reloj. Para obtener más información, vea [Relojes de referencia.](reference-clocks.md)
-   En relación con el inicio de la reproducción.

Para obtener más información sobre las horas de referencia, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Strmif.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Tipos de datos](directshow-data-types.md)
</dt> </dl>

 

 




