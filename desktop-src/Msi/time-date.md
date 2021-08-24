---
description: El tipo de datos Time/Date tiene la hora y la fecha almacenadas individualmente, usando enteros sin signo como campos de bits, empaquetados como se muestra a continuación.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date (Fecha y hora)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810745"
---
# <a name="timedate"></a>Time/Date (Fecha y hora)

El tipo de datos Time/Date tiene la hora y la fecha almacenadas individualmente, usando enteros sin signo como campos de bits, empaquetados como se muestra a continuación.

## <a name="time"></a>Time

La hora se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.



| Contenido           | Bits        | Intervalo de valores |
|--------------------|-------------|-------------|
| horas              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| Intervalos de 2 segundos | B C D E F   | 0–29        |



 

## <a name="date"></a>Date

Date se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.



| Contenido | Bits          | Intervalo de valores              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0–119 (con respecto a 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



