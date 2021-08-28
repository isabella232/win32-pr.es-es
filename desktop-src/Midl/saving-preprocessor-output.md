---
title: Guardar la salida del preprocesador
description: Ver la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C no válida, o cuando los valoresus -D de la línea de comandos MIDL dan lugar a errores arcanos de midl.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL del compilador MIDL, guardar la salida del preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f016885ac4d669d7b62eaf3ff1d5ee3154f03d5eae64fca5f63c6111dff4c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641380"
---
# <a name="saving-preprocessor-output"></a>Guardar la salida del preprocesador

Ver la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C no válida, o cuando los valoresus -D de la línea de comandos MIDL dan lugar a errores arcanos de midl. Es posible que los desarrolladores también quieran examinar la salida del preprocesador para determinar qué archivos y definiciones estaban presentes en el flujo de entrada del compilador, por ejemplo, cuando se debe resolver un caso difícil de conflicto de redefinición de tipos. O menos habitualmente, es posible que determinados desarrolladores quieran forzar conmutadores privados en el preprocesador con [**/cpp \_ opt**](-cpp-opt.md)o que quieran ver cómo funcionan los conmutadores.

La manera más fácil y menos obtrusiva de obtener los archivos preprocesados de una ejecución de compilación MIDL es usar el [**modificador -savePP.**](-savepp.md) El **modificador -savePP** simplemente impide que MIDL elimine los archivos temporales que el preprocesador pasa a MIDL. Tenga en cuenta lo siguiente.

**midl -savePP -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 -Oicf -env win32 stub.idl**

Esta directiva compila Stub.idl, pero conserva todos los archivos de preprocesador.

> [!Note]  
> MIDL genera ejecuciones de preprocesador independientes para el archivo IDL y ACF (si existe), así como para cada archivo importado.

 

En el caso de una compilación DCOM, se suelen generar varios archivos de preprocesador, aunque MIDL los procese como un flujo de entrada contiguo virtual. En un entorno Windows programación, los archivos temporales se pueden encontrar en el directorio Temp como nombres de archivo como MID \* .tmp. Si se conserva la salida del preprocesador, es una buena práctica observar los archivos recientes en el directorio Temp para identificar qué archivos están asociados con qué preprocesador se ejecutan.

En casos simples, como cuando el archivo IDL compilado no importa otros archivos directa o indirectamente, o al examinar el archivo de nivel superior, el preprocesador se puede invocar directamente. Ejecutar directamente el preprocesador de C/C++ puede revelar errores enmascarados o confusos por MIDL. Por ejemplo, se pueden usar las dos líneas de comandos de preprocesador siguientes para la línea MIDL entrecomillada anteriormente:

**cl /E /nologo -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl > stub.pp**

**cl /E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl**

En el primero de estos dos ejemplos, **/E** [**/nologo**](-nologo.md) son los modificadores que MIDL agrega al invocar el preprocesador. La salida del preprocesador se envía a stdout (la pantalla) y, por tanto, requiere el redireccionamiento a un archivo para su examen. En el segundo de estos ejemplos, **/P** dirige al preprocesador para redirigir la salida a un archivo .i; en este caso, se crearía un archivo Stub.i en el \* directorio actual.

El [**modificador /cpp \_ opt**](-cpp-opt.md) también se puede usar para obtener un archivo preprocesado, pero es difícil e inferior a los métodos mencionados anteriormente. En el ejemplo siguiente también se genera un archivo Stub.i, al igual que en el ejemplo anterior. Las comillas del ejemplo siguiente son esenciales:

**Midl -Oicf -win32 -cpp \_ opt "/E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1" stub.idl**

 

 




