---
description: Prevención de ejecución de datos (DEP) es una característica de protección de memoria de nivel de sistema integrada en el sistema operativo a partir de Windows XP y Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Prevención de ejecución de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159876"
---
# <a name="data-execution-prevention"></a>Prevención de ejecución de datos

Prevención de ejecución de datos (DEP) es una característica de protección de memoria de nivel de sistema integrada en el sistema operativo a partir de Windows XP y Windows Server 2003. DEP permite al sistema marcar una o varias páginas de memoria como no ejecutables. Marcar las regiones de memoria como no ejecutables significa que el código no se puede ejecutar desde esa región de memoria, lo que dificulta la explotación de las saturaciones del búfer.

DEP impide que el código se ejecute desde páginas de datos, como el montón predeterminado, las pilas y los grupos de memoria. Si una aplicación intenta ejecutar código desde una página de datos protegida, se produce una excepción de infracción de acceso a la memoria y, si no se controla la excepción, finaliza el proceso de llamada.

DEP no pretende ser una defensa completa contra todas las vulnerabilidades de seguridad. está pensado para ser otra herramienta que puede usar para proteger la aplicación.

## <a name="how-data-execution-prevention-works"></a>Funcionamiento de la prevención de ejecución de datos

Si una aplicación intenta ejecutar código desde una página protegida, la aplicación recibe una excepción con el código de estado **STATUS \_ ACCESS \_ VIOLATION**. Si la aplicación debe ejecutar código desde una página de memoria, debe asignar y establecer los atributos de protección de memoria virtual [adecuados.](memory-protection.md) La memoria asignada debe marcarse como **PAGE \_ EXECUTE,** **PAGE EXECUTE \_ \_ READ,** **PAGE EXECUTE \_ \_ READWRITE** o **PAGE EXECUTE \_ \_ WRITECOPY** al asignar memoria. Las asignaciones de montón realizadas mediante una llamada a las funciones **malloc** y [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) no son ejecutables.

Las aplicaciones no pueden ejecutar código desde el montón de procesos predeterminado o la pila.

DEP se configura en el arranque del sistema según la configuración de directiva de protección de páginas no ejecutada en los datos de configuración de arranque. Una aplicación puede obtener la configuración de directiva actual llamando a la [**función GetSystemDEPPolicy.**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) En función de la configuración de directiva, una aplicación puede cambiar la configuración de DEP para el proceso actual llamando a la [**función SetProcessDEPPolicy.**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy)

## <a name="programming-considerations"></a>Consideraciones sobre la programación

Una aplicación puede usar la [**función VirtualAlloc para**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) asignar memoria ejecutable con las opciones de protección de memoria adecuadas. Se recomienda que una aplicación establezca, como mínimo, la opción de protección de memoria **PAGE \_ EXECUTE.** Una vez generado el código ejecutable, se recomienda que la aplicación establezca protecciones de memoria para no permitir el acceso de escritura a la memoria asignada. Las aplicaciones pueden no permitir el acceso de escritura a la memoria asignada mediante la [**función VirtualProtect.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) No permitir el acceso de escritura garantiza la máxima protección para las regiones ejecutables del espacio de direcciones del proceso. Debe intentar crear aplicaciones que usen el menor espacio de direcciones ejecutable posible, lo que minimiza la cantidad de memoria expuesta a la explotación de memoria.

También debe intentar controlar el diseño de la memoria virtual de la aplicación y crear regiones ejecutables. Estas regiones ejecutables deben estar ubicadas en un espacio de memoria inferior que las regiones no ejecutables. Al buscar regiones ejecutables debajo de regiones no ejecutables, puede ayudar a evitar que un desbordamiento de búfer se desborde en el área ejecutable de memoria.

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

Algunas funcionalidades de la aplicación no son compatibles con DEP. Las aplicaciones que realizan la generación dinámica de código (como la generación de código Just-In-Time) y no marcan explícitamente el código generado con permiso de ejecución pueden tener problemas de compatibilidad en equipos que usan DEP. Las aplicaciones escritas en la versión 7.1 de Active Template Library (ATL) y versiones anteriores pueden intentar ejecutar código en páginas marcadas como no ejecutables, lo que desencadena un error NX y finaliza la aplicación. Para obtener más información, [**vea SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). La mayoría de las aplicaciones que realizan acciones incompatibles con DEP deben actualizarse para funcionar correctamente.

Un pequeño número de bibliotecas y archivos ejecutables puede contener código ejecutable en la sección de datos de un archivo de imagen. En algunos casos, las aplicaciones pueden colocar pequeños segmentos de código (normalmente denominados thunks) en las secciones de datos. Sin embargo, DEP marca las secciones del archivo de imagen que se cargan en memoria como no ejecutables, a menos que la sección tenga aplicado el atributo ejecutable.

Por lo tanto, el código ejecutable de las secciones de datos debe migrarse a una sección de código o la sección de datos que contiene el código ejecutable debe marcarse explícitamente como ejecutable. El atributo **ejecutable, IMAGE \_ SCN \_ MEM \_ EXECUTE,** debe agregarse al campo **Características** del encabezado de sección correspondiente para las secciones que contienen código ejecutable. Para más información sobre cómo agregar atributos a una sección, consulte la documentación incluida con el vinculador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prevención de ejecución de datos (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Configuración de la protección de memoria](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[Artículo de KB 875352](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
