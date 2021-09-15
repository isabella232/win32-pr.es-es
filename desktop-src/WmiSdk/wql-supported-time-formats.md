---
description: Describe los formatos de hora admitidos para su uso en la cláusula WHERE de WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569680"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported de tiempo

Además del formato DATETIME de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula WHERE de WQL.



| Formato                                    | Descripción                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP}M<br/>                   | Hora tal como se muestra en un reloj de doce horas y designación de AM o PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Hora y minutos delimitados por dos puntos. Sin designación de AM o PM.<br/> 3:23<br/>                                                                                                                  |
| hh:mm \[ \] {AP}M<br/>                | Hora y minutos delimitados por dos puntos, espacio opcional y designación de AM o PM.<br/> 3:23 a. m.<br/>                                                                                              |
| hh:mm:ss<br/>                       | Hora, minutos y segundos delimitados por dos puntos. No designación de AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh:mm:ss \[ \] {AP}M<br/>             | Hora, minutos y segundos delimitados por dos puntos, espacio opcional y designación de AM/PM.<br/> 3:23:00 p. m.<br/>                                                                                      |
| hh:mm:ss:uuu<br/>                   | Hora delimitada por dos puntos, minutos y segundos, y desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc.<br/>                                    |
| hh:mm:ss: \[ \[ u u \] \] u<br/>           | Hora, minutos y segundos delimitados por dos puntos; y un desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc.<br/>                       |
| hh:mm:ss:uuu \[ \] {AP}M<br/>         | Hora, minutos y segundos delimitados por dos puntos, desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc y designación de AM o PM.<br/>              |
| hh:mm:ss: \[ \[ u u u \] \] \[ \] {AP}M<br/> | Hora, minutos y segundos delimitados por dos puntos; desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de utc; y designación de AM o PM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




