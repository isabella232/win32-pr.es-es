---
description: La prevención de ejecución de datos (DEP) es una característica de protección de memoria de nivel de sistema integrada en el sistema operativo a partir de Windows XP y Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Prevención de ejecución de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677777"
---
# <a name="data-execution-prevention"></a>Prevención de ejecución de datos

La prevención de ejecución de datos (DEP) es una característica de protección de memoria de nivel de sistema integrada en el sistema operativo a partir de Windows XP y Windows Server 2003. DEP permite que el sistema Marque una o más páginas de memoria como no ejecutables. Marcar regiones de memoria como no ejecutables significa que el código no se puede ejecutar desde esa región de memoria, lo que dificulta la explotación de saturaciones del búfer.

DEP impide que el código se ejecute desde páginas de datos como el montón predeterminado, las pilas y los grupos de memoria. Si una aplicación intenta ejecutar código desde una página de datos que está protegida, se produce una excepción de infracción de acceso a la memoria y, si la excepción no se controla, se termina el proceso de llamada.

DEP no pretende ser una defensa completa contra todas las vulnerabilidades; está pensado para ser otra herramienta que puede usar para proteger su aplicación.

## <a name="how-data-execution-prevention-works"></a>Cómo funciona la prevención de ejecución de datos

Si una aplicación intenta ejecutar código desde una página protegida, la aplicación recibe una excepción con el estado de código **\_ \_ infracción de acceso**. Si la aplicación debe ejecutar código desde una página de memoria, debe asignar y establecer los atributos adecuados de [protección de memoria](memory-protection.md) virtual. La memoria asignada debe estar marcada como **\_ Ejecutar página**, **página \_ ejecutar \_ lectura**, **página \_ ejecutar \_ ReadWrite** o **página \_ ejecutar \_ WRITECOPY** al asignar memoria. Las asignaciones del montón realizadas llamando a las funciones **malloc** y [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) no son ejecutables.

Las aplicaciones no pueden ejecutar código del montón de proceso predeterminado o de la pila.

DEP se configura en el arranque del sistema según la configuración de la Directiva de protección de página sin ejecutar en los datos de la configuración de arranque. Una aplicación puede obtener la configuración de directiva actual mediante una llamada a la función [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) . En función de la configuración de la Directiva, una aplicación puede cambiar la configuración de DEP para el proceso actual llamando a la función [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) .

## <a name="programming-considerations"></a>Consideraciones sobre la programación

Una aplicación puede usar la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) para asignar memoria ejecutable con las opciones de protección de memoria adecuadas. Se recomienda que una aplicación establezca, como mínimo, la opción de protección de memoria de la **página \_ Ejecutar** . Una vez generado el código ejecutable, se recomienda que la aplicación establezca protecciones de memoria para no permitir el acceso de escritura a la memoria asignada. Las aplicaciones pueden impedir el acceso de escritura a la memoria asignada mediante la función [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) . Si no se permite el acceso de escritura, se garantiza la protección máxima para las regiones ejecutables del espacio de direcciones de proceso. Debe intentar crear aplicaciones que usen el menor espacio de direcciones ejecutable posible, lo que minimiza la cantidad de memoria expuesta a la explotación de la memoria.

También debe intentar controlar el diseño de la memoria virtual de la aplicación y crear regiones ejecutables. Estas regiones ejecutables se deben ubicar en un espacio de memoria inferior al de las regiones no ejecutables. Al buscar regiones ejecutables por debajo de regiones no ejecutables, puede ayudar a evitar que se produzca un desbordamiento del búfer en el área de memoria ejecutable.

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

Alguna funcionalidad de la aplicación no es compatible con DEP. Las aplicaciones que realizan la generación dinámica de código (como la generación de código Just-in-Time) y no marcan explícitamente el código generado con el permiso Execute pueden tener problemas de compatibilidad en los equipos que usan DEP. Las aplicaciones escritas en la versión 7,1 de Active Template Library (ATL) y versiones anteriores pueden intentar ejecutar código en páginas marcadas como no ejecutables, lo que desencadena un error de NX y finaliza la aplicación; para obtener más información, vea [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). La mayoría de las aplicaciones que realizan acciones incompatibles con DEP deben actualizarse para funcionar correctamente.

Un pequeño número de bibliotecas y archivos ejecutables puede contener código ejecutable en la sección de datos de un archivo de imagen. En algunos casos, las aplicaciones pueden colocar pequeños segmentos de código (denominados comúnmente como thunks) en las secciones de datos. Sin embargo, DEP marca las secciones del archivo de imagen que se cargan en memoria como no ejecutables a menos que la sección tenga aplicado el atributo ejecutable.

Por lo tanto, el código ejecutable de las secciones de datos se debe migrar a una sección de código, o la sección de datos que contiene el código ejecutable debe marcarse explícitamente como ejecutable. El atributo ejecutable, **Image \_ SCN \_ MEM \_ Execute**, debe agregarse al campo **Characteristics** del encabezado de sección correspondiente para las secciones que contienen código ejecutable. Para obtener más información sobre cómo agregar atributos a una sección, consulte la documentación que se incluye con el enlazador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prevención de ejecución de datos (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Cómo configurar la protección de memoria](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[Artículo de KB 875352](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
