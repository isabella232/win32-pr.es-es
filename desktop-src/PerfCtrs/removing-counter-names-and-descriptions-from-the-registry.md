---
description: La herramienta unlodctr quita las entradas del Registro creadas por lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Quitar nombres y descripciones de contadores del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c086520f1fb261a0b9850c03f2aee28065a03ee514df277fbf1cae602deed6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962355"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Quitar nombres y descripciones de contadores del Registro

La **herramienta unlodctr** quita las entradas del Registro creadas por **lodctr**. El nombre de la aplicación que pase **a unlodctr** debe coincidir con el nombre de la clave de [aplicación](creating-the-applications-performance-key.md) que creó en la **clave Servicios.** Para más información sobre **cómo ejecutar unlodctr,** consulte Centro de ayuda y soporte técnico.

## <a name="using-unlodctr"></a>Uso de unlodctr

La **herramienta unlodctr** busca el primer y último contador y ayuda a indexar los valores mediante los valores del Registro con nombre similar en la clave **de rendimiento de la** aplicación. La **herramienta unlodctr** usa el intervalo de  valores de índice para quitar el texto de contadores y valores **de** Ayuda para cada identificador de idioma.

Con los valores de índice, **unlodctr** realiza los siguientes cambios en el registro.

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

La herramienta **unlodctr** también quita los valores First **Counter**, Last **Counter**, First  **Help**, **Last Help** y **Object List** de la clave de rendimiento de la aplicación ubicada en **HKEY LOCAL \_ \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *application-name* \\ **Performance**.

> [!Note]  
> La función de descarga **de unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), se declara en Loadperf.h y se exporta desde Loadperf.dll. Esto le permite llamar a esta función directamente desde el programa de desinstalación.

 

 

 



