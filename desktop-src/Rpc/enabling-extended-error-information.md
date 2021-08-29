---
title: Habilitación de la información de error extendida
description: Habilitar la información de error extendida para la llamada a procedimiento remoto (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0813e770a6b1490ddd3e8e90b050f575ee76d01cf8e4e5d59b4d9e0eff74ce2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021675"
---
# <a name="enabling-extended-error-information"></a>Habilitación de la información de error extendida

Para habilitar la información de error extendida, siga estos pasos:

Abra la directiva de máquina local mediante la interfaz gpedit.msc.

Vaya a la directiva que se encuentra en Configuración del equipo/Plantillas administrativas/Sistema/Llamada a procedimiento remoto/Compatibilidad con la solución de problemas rpc/propagación de información de error extendida

Habilite la directiva y establezca el campo **Propagación de la información de error extendida** en "On".

Este proceso activa la propagación de información de error extendida para todos los procesos de la máquina.

Para habilitar la información de error extendida solo para **determinados** procesos de un equipo o para deshabilitarla solo para **determinados** procesos del equipo, use las opciones Desactivado con excepciones o Activar con excepciones. Ambas opciones usan el campo **Excepciones de** información de error extendida para especificar qué procesos tienen la configuración predeterminada y qué procesos tienen lo contrario que la configuración predeterminada. **Excepciones de información de error extendida contiene** una lista de nombres de proceso.

Si la línea de comandos de un proceso comienza con una cadena que se encuentra en las excepciones de información de **error** extendida, el proceso recibirá lo contrario de la configuración predeterminada. Por ejemplo, si desea que todo el proceso del equipo propague información de error extendida, excepto lsass y el proceso denominado **Servidor** seguro , establezca la propagación de información de **error** extendida en **On con** excepciones y especifique en el campo Excepciones de información de error extendida **la** cadena siguiente: lsass "Servidor seguro".

Las cadenas se pueden incluir entre comillas dobles, pero es opcional si no hay espacios en la cadena. Además, se puede especificar el principio de la línea de comandos del proceso. Por ejemplo, si se especifica **Desactivado** con excepciones en el campo  Propagación de información **de error** extendida y en el campo Excepciones de información de error extendida se especifica lo siguiente: win.

Cada proceso que comienza con "win" propaga información de error extendida. En muchos equipos, por ejemplo, esos procesos se winlogon.exe y WINWORD.EXE.

 

 




