---
description: Describe los formatos de tiempo admitidos para su uso en la cláusula WHERE de WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627b46ef7d01a2eb3e8e40484b37822c9ebca55a9487b1ffb0e1a138ab7378d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049743"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported de tiempo

Además del formato DATETIME de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula WHERE de WQL.



| Formato                                    | Descripción                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP}M<br/>                   | Hora como se muestra en un reloj de doce horas y designación de AM o PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Hora y minutos delimitados por dos puntos. Sin designación de AM o PM.<br/> 3:23<br/>                                                                                                                  |
| hh:mm \[ \] {AP}M<br/>                | Hora y minutos delimitados por dos puntos, espacio opcional y designación de AM o PM.<br/> 3:23 a. m.<br/>                                                                                              |
| hh:mm:ss<br/>                       | Hora, minutos y segundos delimitados por dos puntos. Sin designación de AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh:mm:ss \[ \] {AP}M<br/>             | Hora, minutos y segundos delimitados por dos puntos, espacio opcional y designación de AM/PM.<br/> 3:23:00 p. m.<br/>                                                                                      |
| hh:mm:ss:uuu<br/>                   | Hora, minutos y segundos delimitados por dos puntos y un desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc.<br/>                                    |
| hh:mm:ss: \[ \[ u u \] \] u<br/>           | Hora, minutos y segundos delimitados por dos puntos; y un desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc.<br/>                       |
| hh:mm:ss:uuu \[ \] {AP}M<br/>         | Hora delimitada por dos puntos, minutos y segundos, desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc y la designación de AM o PM.<br/>              |
| hh:mm:ss: \[ \[ u u u \] \] \[ \] {AP}M<br/> | Hora, minutos y segundos delimitados por dos puntos; desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc; y designación de AM o PM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




