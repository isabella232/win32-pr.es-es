---
title: Habilitar información de error extendida
description: Habilitar la información de error extendida para la llamada a procedimiento remoto (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269033"
---
# <a name="enabling-extended-error-information"></a>Habilitar información de error extendida

Para habilitar la información de error extendida, siga estos pasos:

Abra la Directiva del equipo local mediante la interfaz gpedit. msc.

Vaya a la Directiva que se encuentra en configuración del equipo/Plantillas administrativas/sistema/llamada a procedimiento remoto/compatibilidad con la solución de problemas de RPC/propagación de la información de error extendida.

Habilite la Directiva y establezca la **propagación del campo de información de error extendida** en "activado".

Este proceso convierte la propagación de la información de error extendida en para todos los procesos del equipo.

Para habilitar la información de error extendida solo para determinados procesos de un equipo, o para deshabilitarlo solo en determinados procesos del equipo, use las opciones **desactivado con excepciones** o **con excepciones** . Ambas opciones usan las **excepciones de información de errores extendidos** de campo para especificar los procesos que tienen la configuración predeterminada y los procesos que tienen la misma configuración predeterminada. **Excepciones de información de error extendida** contiene una lista de nombres de proceso.

Si la línea de comandos de un proceso comienza con una cadena que se encuentra en las **excepciones de información de error extendida**, el proceso recibirá la configuración predeterminada. Por ejemplo, si desea que todo el proceso del equipo propague información extendida de errores, excepto para LSASS y el proceso llamado **servidor seguro**, establezca la **propagación de la información de errores extendida** en **activado con excepciones** y especifique en el campo **excepciones de información de error extendida** la siguiente cadena: LSASS "servidor seguro".

Las cadenas se pueden incluir entre comillas dobles, pero es opcional si no hay ningún espacio en la cadena. Además, se puede especificar el principio de la línea de comandos del proceso. Por ejemplo, si se especifica **OFF con excepciones** en el campo **propagación de información de error extendida** , y en el campo **excepciones de información de error extendida** se especifica lo siguiente: Win.

Cada proceso que comienza por "Win" propaga información de error extendida. En muchos equipos, por ejemplo, estos procesos se winlogon.exe y WINWORD.EXE.

 

 




