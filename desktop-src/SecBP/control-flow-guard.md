---
description: La protección de flujo de control (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para combatir vulnerabilidades de daños en la memoria.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Protección de flujo de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156869"
---
# <a name="control-flow-guard"></a>Protección de flujo de control

## <a name="what-is-control-flow-guard"></a>¿Qué es la protección de flujo de control?

La protección de flujo de control (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para combatir vulnerabilidades de daños en la memoria. Al colocar restricciones estrictas en el lugar desde el que una aplicación puede ejecutar código, resulta mucho más difícil para los ataques ejecutar código arbitrario a través de vulnerabilidades como desbordamientos del búfer. CFG amplía las tecnologías de mitigación de vulnerabilidades anteriores, como [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md)y [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).

Esta característica está disponible en Microsoft Visual Studio 2015 y se ejecuta en las versiones de Windows "compatibles con CFG": las versiones x86 y x64 para Desktop y Server de Windows 10 y Windows 8.1 Update (KB3000850).

Recomendamos encarecidamente que los desarrolladores habiliten CFG para sus aplicaciones. No tiene que habilitar CFG para todas las partes del código, ya que se ejecutará correctamente una combinación de CFG habilitada y el código no compatible con CFG. Pero si no se habilita CFG para todo el código, pueden abrirse brechas en la protección. Además, el código habilitado para CFG funciona correctamente en las versiones de Windows que no son compatibles con CFG y, por lo tanto, es totalmente compatible con ellos.

## <a name="how-can-i-enable-cfg"></a>¿Cómo se puede habilitar CFG?

En la mayoría de los casos, no es necesario cambiar el código fuente. Lo único que tiene que hacer es agregar una opción al proyecto de Visual Studio 2015 y el compilador y el vinculador habilitarán CFG.

El método más sencillo consiste en ir a propiedades de **configuración del proyecto \| generación de \| \| \| código C/C++** y elegir **sí (/Guard: CF)** para la protección de flujo de control.

![propiedad cfg en Visual Studio](images/cfg-vs.png)

Como alternativa, agregue **/Guard: CF** a propiedades de **configuración del proyecto \| Opciones de configuración de línea de \| \| \| comandos \| de C/C++** (para el compilador) y **/Guard: CF** a propiedades de configuración propiedades de la **línea de \| \| \| comandos del vinculador \| \| opciones adicionales** (para el vinculador).

![propiedad cfg del compilador](images/cfg-compiler.png)![propiedad cfg para el vinculador](images/cfg-linker.png)

Consulte [/Guard (habilitar protección de flujo de control)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) para obtener información adicional.

Si va a compilar el proyecto desde la línea de comandos, puede Agregar las mismas opciones. Por ejemplo, si va a compilar un proyecto denominado test. cpp, use **cl/Guard: CF test. cpp/Link/Guard: CF**.

También tiene la opción de controlar dinámicamente el conjunto de direcciones de destino de iCall que se considera válidas en CFG mediante [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) desde la API de administración de memoria. Se puede usar la misma API para especificar si las páginas no son válidas o son destinos válidos para CFG. De forma predeterminada, las funciones [**VirtualProtect (**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) y [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) tratarán una región específica de páginas ejecutables y confirmadas como destinos de llamada indirecta válidos. Es posible invalidar este comportamiento (por ejemplo, al implementar un compilador Just-in-Time) mediante la especificación de **destinos de página \_ \_ no válidos** al llamar a **VirtualAlloc** o los destinos de la **página \_ no se \_ \_ actualizan** al llamar a **VirtualProtect (** , tal y como se detalla en las constantes de [**protección de memoria**](/windows/desktop/Memory/memory-protection-constants).

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>¿Cómo se puede saber que un archivo binario está en la protección del flujo de control?

Ejecute la [herramienta DUMPBIN](/cpp/build/reference/dumpbin-reference) (incluida en la instalación de visual Studio 2015) desde el símbolo del sistema de Visual Studio con las opciones */headers* y */loadconfig* : **dumpbin/headers/loadconfig test.exe**. La salida de un archivo binario en CFG debe mostrar que los valores de encabezado incluyen "Guard", y que los valores de configuración de carga incluyen "CF instrumentado" y "tabla de FID presente".

![salida de DUMPBIN/headers](images/cfg-dumpbin-headers.png)

![resultado de DUMPBIN/loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>¿Cómo funciona CFG realmente?

A menudo, las vulnerabilidades de software se aprovechan al proporcionar datos poco probables, inusuales o extremos a un programa en ejecución. Por ejemplo, un atacante puede aprovechar una vulnerabilidad de desbordamiento de búfer al proporcionar más información a un programa de la esperada, con lo que se ejecuta en exceso el área reservada por el programa para contener una respuesta. Esto podría dañar la memoria adyacente que puede contener un puntero de función. Cuando el programa llama a través de esta función, puede saltar a una ubicación no deseada especificada por el atacante.

Sin embargo, una combinación potente de compatibilidad de compilación y en tiempo de ejecución de CFG implementa la integridad del flujo de control que se restringe estrictamente donde se pueden ejecutar instrucciones de llamadas indirectas.

El compilador hace lo siguiente:

1.  Agrega comprobaciones de seguridad ligeras al código compilado.
2.  Identifica el conjunto de funciones de la aplicación que son destinos válidos para las llamadas indirectas.

Compatibilidad en tiempo de ejecución, proporcionada por el kernel de Windows:

1.  Mantiene eficazmente el estado que identifica los destinos de llamada indirecta válidos.
2.  Implementa la lógica que comprueba que un destino de llamada indirecto es válido.

Para ilustrar:

![pseudocódigo de cfg](images/cfg-pseudocode.jpg)

Cuando se produce un error en una comprobación de CFG en tiempo de ejecución, Windows finaliza inmediatamente el programa, con lo que se interrumpe cualquier ataque que intente llamar indirectamente a una dirección no válida.

 

 
