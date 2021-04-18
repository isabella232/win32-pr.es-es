---
description: La herramienta Unlodctr quita las entradas del registro creadas por LODCTR.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Quitar nombres y descripciones de contadores del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667252"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Quitar nombres y descripciones de contadores del registro

La herramienta **Unlodctr** quita las entradas del registro creadas por **LODCTR**. El nombre de la aplicación que pase a **Unlodctr** debe coincidir con el [nombre de la clave de aplicación](creating-the-applications-performance-key.md) que creó en la clave **servicios** . Para obtener más información sobre cómo ejecutar **Unlodctr** , vea el centro de ayuda y soporte técnico.

## <a name="using-unlodctr"></a>Usar Unlodctr

La herramienta **Unlodctr** busca el primer y último contador y los valores de índice de la ayuda usando los valores del registro con el mismo nombre en la clave de **rendimiento** de la aplicación. La herramienta **Unlodctr** usa el intervalo de valores de índice para quitar el texto de los **contadores** y los valores de **ayuda** de cada identificador de idioma.

Con los valores de índice, **Unlodctr** realiza los siguientes cambios en el registro.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

La herramienta **Unlodctr** también quita los valores del **primer contador**, **último contador**, **primera ayuda**, **última ayuda** y **lista de objetos** de la clave de **rendimiento** de la aplicación que se encuentra en **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.

> [!Note]  
> La función de descarga de **Unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), se declara en Loadperf. h y se exporta desde Loadperf.dll. Esto le permite llamar a esta función directamente desde el programa de desinstalación.

 

 

 



