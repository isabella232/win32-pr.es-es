---
description: Describe los formatos de hora admitidos para su uso en la cláusula WQL WHERE.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formatos de hora de WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715817"
---
# <a name="wql-supported-time-formats"></a>Formatos de hora de WQL-Supported

Además del formato DATETIME de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula WHERE de WQL.



| Formato                                    | Descripción                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HH \[ \] {AP} M<br/>                   | Hora, tal como se muestra en un reloj de 12 horas, y la designación AM o PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Hora y minutos delimitados por signos de dos puntos. Sin designación AM o PM.<br/> 3:23<br/>                                                                                                                  |
| HH: mm \[ \] {AP} M<br/>                | Horas y minutos delimitados por signos de dos puntos, espacio opcional y designación AM o PM.<br/> 3:23 AM<br/>                                                                                              |
| hh:mm:ss<br/>                       | Hora, minutos y segundos delimitados por signos de dos puntos. Ninguna designación AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| HH: mm: SS \[ \] {AP} M<br/>             | Hora, minutos y segundos delimitados por signos de dos puntos, espacio opcional y designación AM/PM.<br/> 3:23: P.M.<br/>                                                                                      |
| HH: mm: SS: UUU<br/>                   | Hora, minutos y segundos delimitados por signos de dos puntos, y desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC.<br/>                                    |
| HH: mm: SS: \[ \[ u \] u \] u<br/>           | Hora, minutos y segundos delimitados por signos de dos puntos; y un desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC.<br/>                       |
| HH: mm: SS: UUU \[ \] {AP} M<br/>         | Hora, minutos y segundos delimitados por signos de dos puntos, desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC y la designación AM o PM.<br/>              |
| HH: mm: SS: \[ \[ u \] u \] u \[ \] {AP} M<br/> | Hora, minutos y segundos delimitados por signos de dos puntos; desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC. y la designación AM o PM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




