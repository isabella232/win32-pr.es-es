---
description: CONFIGURACIÓN REGIONAL \_ DE LA CONFIGURACIÓN REGIONAL
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb7031c5e9ddc3173fe7f10117eaad8c72820b1d3b81a82da33f6541901a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147368"
---
# <a name="locale_sduration"></a>CONFIGURACIÓN REGIONAL \_ DE LA CONFIGURACIÓN REGIONAL

**Windows Vista y versiones posteriores:** Formato de duración de tiempo compuesto por imágenes de formato enumeradas en la tabla siguiente. El formato es similar al formato de [LOCALE \_ STIMEFORMAT](locale-stime-constants.md). En cuanto a LOCALE STIMEFORMAT, este formato también puede incluir cualquier \_ cadena de caracteres entre comillas simples. Los formatos pueden incluir, por ejemplo, "h:mm:ss" o "d'd 'h'h 'm'm 's.fff's'". En comparación con LOCALE STIMEFORMAT, hay imágenes de formato adicionales \_ para fracciones de segundo. Dado que este formato es de duración, no de tiempo, no especifica un sistema de reloj de 12 o 24 horas, ni incluye un indicador am/PM. Esta constante se puede usar, por ejemplo, para una aplicación multi multimedia que muestra la hora del archivo o una aplicación de eventos deportivos que muestra los tiempos de terminación.



| Value | Significado                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Horas sin ceros iniciales para horas de un solo dígito                                                                                                                                                                                  |
| hh    | Horas con ceros a la izquierda para horas de un solo dígito                                                                                                                                                                                     |
| m     | Minutos sin ceros iniciales para minutos de un solo dígito                                                                                                                                                                              |
| MM    | Minutos con ceros a la izquierda para minutos de un solo dígito                                                                                                                                                                                 |
| s     | Segundos sin ceros iniciales para segundos de un solo dígito                                                                                                                                                                              |
| ss    | Segundos con ceros iniciales para segundos de un solo dígito                                                                                                                                                                                 |
| f     | Décimas de segundo                                                                                                                                                                                                                  |
| ff    | Centésimas de segundo                                                                                                                                                                                                              |
| fff   | Milésimas de segundo; el carácter "f" puede producirse hasta nueve veces consecutivas (fffffffff), aunque la compatibilidad con temporizadores de frecuencia está limitada a 100 nanosegundos. si hay nueve caracteres, los dos últimos dígitos siempre son cero |



 

 

 



