---
title: Guardar la salida del preprocesador
description: La visualización de la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C, o cuando los valores fantasma en la línea de comandos de MIDL dan como resultado errores de los informes de MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL del compilador MIDL, guardar la salida del preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418817"
---
# <a name="saving-preprocessor-output"></a>Guardar la salida del preprocesador

La visualización de la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C, o cuando los valores fantasma en la línea de comandos de MIDL dan como resultado errores de los informes de MIDL. Los desarrolladores también pueden querer examinar la salida del preprocesador para determinar qué archivos y definiciones estaban presentes en el flujo de entrada del compilador, por ejemplo, cuando se debe resolver un caso difícil de conflicto de redefinición de tipo. O menos comúnmente, algunos desarrolladores pueden querer forzar los conmutadores privados en el preprocesador con [**/CPP \_ OPT**](-cpp-opt.md), o bien, puede que desee ver cómo funcionan los conmutadores.

La forma más sencilla y molesta de obtener los archivos preprocesados de una ejecución de compilación de MIDL es usar el modificador [**-savePP**](-savepp.md) . El modificador **-savePP** simplemente impide que MIDL elimine los archivos temporales que el preprocesador pasa de nuevo a MIDL. Tenga en cuenta lo siguiente.

**MIDL-savePP-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**

Esta directiva compila stub. idl, conserva todos los archivos de preprocesador.

> [!Note]  
> MIDL genera ejecuciones de preprocesador independientes para archivos IDL y ACF (si existen), así como para todos los archivos importados.

 

En el caso de una compilación DCOM, normalmente se generan varios archivos de preprocesador, aunque MIDL los procesa como un flujo de entrada contiguo virtual. En un entorno de programación de Windows típico, los archivos temporales se pueden encontrar en el directorio Temp como nombres de archivo como MID \* . tmp. Si se conserva la salida del preprocesador, se recomienda inspeccionar los archivos recientes en el directorio temporal para identificar qué archivos están asociados con qué ejecución del preprocesador.

En casos sencillos, como cuando el archivo IDL compilado no importa otros archivos directa o indirectamente, o al examinar el archivo de nivel superior, el preprocesador se puede invocar directamente. La ejecución directa del preprocesador de C/C++ puede revelar errores enmascarados o confundidos por MIDL. Por ejemplo, las dos líneas de comandos de preprocesador siguientes se pueden usar para la línea MIDL previamente entrecomillada:

**CL/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**

**CL/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl**

En el primero de estos dos ejemplos, **/e** [**/nologo**](-nologo.md) son los modificadores que MIDL agrega al invocar al preprocesador. La salida del preprocesador se envía a stdout (la pantalla) y, por tanto, requiere la redirección a un archivo para su examen. En el segundo de estos ejemplos, **/p** dirige el preprocesador para redirigir la salida a un \* archivo. i; en este caso, se crearía un archivo stub. i en el directorio actual.

El modificador [**\_ OPT de/CPP**](-cpp-opt.md) también se puede usar para obtener un archivo preprocesado, pero es difícil y inferior a los métodos mencionados anteriormente. En el ejemplo siguiente también se genera un archivo stub. i, como se hizo en el ejemplo anterior. Las comillas en el ejemplo siguiente son esenciales:

**MIDL-Oicf-Win32-CPP \_ OPT "/E/p-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1" stub. idl**

 

 




