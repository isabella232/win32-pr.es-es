---
description: El tipo de datos de fecha y hora tiene la hora y la fecha almacenadas individualmente, utilizando enteros sin signo como campos de bits, empaquetados como se indica a continuación.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date (Fecha y hora)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652733"
---
# <a name="timedate"></a>Time/Date (Fecha y hora)

El tipo de datos de fecha y hora tiene la hora y la fecha almacenadas individualmente, utilizando enteros sin signo como campos de bits, empaquetados como se indica a continuación.

## <a name="time"></a>Hora

La hora se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.



| Contenido           | Bits        | Intervalo de valores |
|--------------------|-------------|-------------|
| horas              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| intervalos de 2 segundos | B C D E F   | de 0 a 29        |



 

## <a name="date"></a>Fecha

La fecha se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.



| Contenido | Bits          | Intervalo de valores              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0 – 119 (con respecto a 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



