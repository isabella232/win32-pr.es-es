---
description: configuración regional \_ SDURATION
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00740d2f041794b36e8f0e0d8ad2d25723bc12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670006"
---
# <a name="locale_sduration"></a>configuración regional \_ SDURATION

**Windows Vista y versiones posteriores:** Formato de duración de tiempo compuesto por las imágenes de formato que aparecen en la tabla siguiente. El formato es similar al formato de la [configuración regional \_ STIMEFORMAT](locale-stime-constants.md). En el caso de \_ la configuración regional STIMEFORMAT, este formato también puede incluir cualquier cadena de caracteres entre comillas simples. Los formatos pueden incluir, por ejemplo, "h:mm: SS" o "d" d "h'h". En comparación con la configuración regional \_ STIMEFORMAT, hay imágenes de formato adicionales para las fracciones de segundo. Dado que este formato es para Duration, no Time, no especifica un sistema de reloj de 12 o 24 horas, ni incluye un indicador AM/PM. Esta constante se puede usar, por ejemplo, para una aplicación de varios medios que muestra la hora de archivo o una aplicación de eventos deportivos que muestra las horas de finalización.



| Value | Significado                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Horas sin ceros a la izquierda para las horas de un solo dígito                                                                                                                                                                                  |
| hh    | Horas con ceros a la izquierda para las horas de un solo dígito                                                                                                                                                                                     |
| m     | Minutos sin ceros a la izquierda para los minutos con un solo dígito                                                                                                                                                                              |
| MM    | Minutos con ceros a la izquierda para los minutos con un solo dígito                                                                                                                                                                                 |
| s     | Segundos sin ceros a la izquierda para los segundos de un solo dígito                                                                                                                                                                              |
| ss    | Segundos con ceros a la izquierda para los segundos de un solo dígito                                                                                                                                                                                 |
| f     | Décimas de segundo                                                                                                                                                                                                                  |
| ff    | Centésimas de segundo                                                                                                                                                                                                              |
| fff   | Milésimas de segundo; el carácter "f" puede tener hasta nueve horas consecutivas (fffffffff), aunque la compatibilidad con los temporizadores de frecuencia está limitada a 100 nanosegundos; Si hay nueve caracteres presentes, los dos últimos dígitos siempre son cero |



 

 

 



