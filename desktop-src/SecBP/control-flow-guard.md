---
description: Control Flow Guard (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para combatir las vulnerabilidades de daños en la memoria.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Protección de flujo de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476543"
---
# <a name="control-flow-guard"></a>Protección de flujo de control

## <a name="what-is-control-flow-guard"></a>¿Qué es Control Flow Guard?

Control Flow Guard (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para combatir las vulnerabilidades de daños en la memoria. Al establecer restricciones estrictas en la ubicación desde la que una aplicación puede ejecutar código, resulta mucho más difícil para las vulnerabilidades ejecutar código arbitrario a través de vulnerabilidades como desbordamientos de búfer. CFG amplía las tecnologías de mitigación de vulnerabilidades anteriores, [como /GS,](/cpp/build/reference/gs-buffer-security-check?view=vs-2019) [DEP](../memory/data-execution-prevention.md)y [ASLR.](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)

Esta característica está disponible en Microsoft Visual Studio 2015 y se ejecuta en versiones "compatibles con CFG" de Windows: las versiones x86 y x64 para escritorio y servidor de Windows 10 y Windows 8.1 Update (KB3000850).

Recomendamos encarecidamente a los desarrolladores que habiliten CFG para sus aplicaciones. No tiene que habilitar CFG para cada parte del código, ya que una combinación de código habilitado para CFG y no habilitado para CFG se ejecutará bien. Pero no habilitar CFG para todo el código puede abrir brechas en la protección. Además, el código habilitado para CFG funciona bien en las versiones "CFG-Unware" de Windows y, por lo tanto, es totalmente compatible con ellas.

## <a name="how-can-i-enable-cfg"></a>¿Cómo se puede habilitar CFG?

En la mayoría de los casos, no es necesario cambiar el código fuente. Todo lo que tiene que hacer es agregar una opción al proyecto de Visual Studio 2015 y el compilador y el vinculador habilitarán CFG.

El método más sencillo es ir a Propiedades de configuración de Project Generación de código **\| \| \| \| C/C++** y elegir **Sí (/guard:cf)** en Control Flow Guard.

![Propiedad cfg en Visual Studio](images/cfg-vs.png)

Como alternativa, agregue **/guard:cf** a propiedades de configuración de Project Opciones adicionales de la línea de comandos **\| de \| \| C/C++ \| \|** (para el compilador) y **/guard:cf** a Project **Propiedades de configuración Del vinculador Opciones adicionales \| \| \| \| \|** de la línea de comandos (para el vinculador).

![Propiedad cfg para el compilador](images/cfg-compiler.png)![Propiedad cfg para el vinculador](images/cfg-linker.png)

Consulte [/guard (Habilitar Control Flow Guard)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) para obtener información adicional.

Si va a compilar el proyecto desde la línea de comandos, puede agregar las mismas opciones. Por ejemplo, si va a compilar un proyecto denominado test.cpp, use **cl /guard:cf test.cpp /link /guard:cf**.

También tiene la opción de controlar dinámicamente el conjunto de direcciones de destino de icall que CFG considera válidas mediante [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) de la memoria API de Administración. Se puede usar la misma API para especificar si las páginas no son válidas o no son destinos válidos para CFG. Las [**funciones VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) y [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) tratarán de forma predeterminada una región especificada de páginas ejecutables y de páginas confirmadas como destinos de llamadas indirectas válidos. Es posible invalidar este comportamiento, como al implementar un compilador Just-In-Time, especificando **PAGE \_ TARGETS \_ INVALID** al llamar a **VirtualAlloc** o **PAGE TARGETS NO \_ \_ \_ UPDATE** al llamar a **VirtualProtect** como se detalla en Constantes de protección de memoria [**.**](/windows/desktop/Memory/memory-protection-constants)

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>¿Cómo puedo saber que un archivo binario está bajo control Flow Guard?

Ejecute la herramienta [dumpbin](/cpp/build/reference/dumpbin-reference) (incluida en la instalación de Visual Studio 2015) desde el símbolo del sistema de Visual Studio con las opciones */headers* y */loadconfig:* **dumpbin /headers /loadconfig test.exe**. La salida de un archivo binario en CFG debe mostrar que los valores de encabezado incluyen "Guard" y que los valores de configuración de carga incluyen "CF Instrumented" y "FID table present".

![salida de dumpbin /headers](images/cfg-dumpbin-headers.png)

![salida de dumpbin /loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>¿Cómo funciona realmente CFG?

Las vulnerabilidades de software a menudo se aprovechan proporcionando datos poco probables, inusuales o extremos a un programa en ejecución. Por ejemplo, un atacante puede aprovechar una vulnerabilidad de desbordamiento de búfer proporcionando más entradas a un programa de las esperadas, con lo que se sobresalte el área reservada por el programa para contener una respuesta. Esto podría dañar la memoria adyacente que puede contener un puntero de función. Cuando el programa llama a través de esta función, puede saltar a una ubicación no deseada especificada por el atacante.

Sin embargo, una combinación perfecta de compatibilidad en tiempo de ejecución y compilación de CFG implementa la integridad del flujo de control que restringe estrechamente dónde se pueden ejecutar las instrucciones de llamada indirecta.

El compilador hace lo siguiente:

1.  Agrega comprobaciones de seguridad ligeras al código compilado.
2.  Identifica el conjunto de funciones de la aplicación que son destinos válidos para las llamadas indirectas.

La compatibilidad en tiempo de ejecución, proporcionada por el Windows kernel:

1.  Mantiene de forma eficaz el estado que identifica destinos de llamadas indirectas válidos.
2.  Implementa la lógica que comprueba que un destino de llamada indirecta es válido.

Para ilustrar:

![Pseudocódigo cfg](images/cfg-pseudocode.jpg)

Cuando se produce un error en una comprobación de CFG en tiempo de ejecución, Windows finaliza inmediatamente el programa, lo que interrumpirá cualquier vulnerabilidad de seguridad que intente llamar indirectamente a una dirección no válida.

 

 
