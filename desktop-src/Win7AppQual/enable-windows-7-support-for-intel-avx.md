---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitar la compatibilidad con Windows 7 para Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697736"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Habilitar la compatibilidad con Windows 7 para Intel AVX

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes** : Windows 7 SP1  
**Servidores** : Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

<sup>¿Intel?</sup> Extensiones de vector avanzadas (AVX<sup>)</sup> es una extensión de vector de punto flotante de 256 bits SIMD de la arquitectura de Intel. Incluye extensiones para los conjuntos de instrucciones y de registro.

Microsoft ha desarrollado algunas mejoras de API, como las funciones de XState, que permiten a las aplicaciones tener acceso y manipular la información y el estado de las características del procesador extendido, incluido AVX.

## <a name="usage-scenarios"></a>Escenarios de uso

Hay tres niveles generales de impacto potencial.

**Nivel 1:** Las aplicaciones que no usan directamente Intel AVX no verán ningún impacto en su funcionalidad, aunque llamen a bibliotecas o usen compiladores que utilicen o generen indirectamente extensiones de Intel AVX. Esto representa la mayoría de las aplicaciones.

**Nivel 2:** Las aplicaciones avanzadas que utilicen explícitamente el conjunto de instrucciones de Intel AVX podrán obtener acceso y cambiar el contenido del registro AVX cuando se produzca una excepción de hardware. Una cantidad muy pequeña de aplicaciones estaría en esta categoría, ya que implica un conocimiento profundo de la secuencia de instrucciones que se ejecuta en el momento de la excepción, como las aplicaciones con secciones escritas en lenguaje ensamblador o las que generan código máquina en tiempo de ejecución (por ejemplo, los tiempos de ejecución de código administrado con la compilación Just-in-Time).

**Nivel 3:** Las aplicaciones del depurador podrán obtener acceso y manipular el estado AVX en la aplicación que se está depurando.

## <a name="how-to-leverage-feature-capabilities"></a>Cómo aprovechar las funcionalidades de características

**Nivel 1:** No es necesario realizar ninguna acción para que las aplicaciones usen Intel AVX.

**Nivel 2:** Las aplicaciones de esta categoría tienen la opción de obtener acceso y manipular el estado AVX en el momento de la excepción desde los filtros de excepciones. Después de obtener el contexto del procesador base a través de GetExceptionInformation, los filtros deben:

 **1.** Compruebe el valor de la **marca \_ XSTATE de contexto** . Esta marca indica la presencia de al menos una característica XState en el contexto.  
**2.** si este es el caso, llame a **GetXStateFeaturesMask** y pruebe el valor de la marca **XSTATE \_ AVX** en la máscara devuelta. Esto indica la presencia del estado AVX en el contexto.  
**3.** llame a **LocateXStateFeature** para recuperar la ubicación real en la que se almacena el estado AVX.  

**Nivel 3:** No es necesario actualizar las aplicaciones del depurador existentes a menos que quieran acceder a los registros AVX de Intel:

**1.** para determinar si AVX está habilitado, el depurador debe usar:

-   GetEnabledXStateFeatures para obtener una máscara de las características habilitadas de XState en procesadores x86 o x64 con el fin de determinar qué características están presentes y habilitadas en el sistema antes de usar una característica de procesador XState o intentar manipular contextos XState

  
**2.** si AVX está presente y desea recuperar y manipular el estado AVX desde la aplicación que se está depurando (por ejemplo, GetThreadContext y SetThreadContext), el depurador debe usar:

-   Función InitializeContext para inicializar una estructura de contexto dentro de un búfer con el tamaño y la alineación necesarios
-   Función CopyContext para copiar una estructura de contexto de origen (incluido cualquier XState) en una estructura de contexto de destino inicializada

  
**3.** para probar, establecer y ubicar el estado AVX en un contexto de procesador, el depurador debe usar:

-   LocateXStateFeature para recuperar un puntero al estado del procesador para una característica XState individual dentro de una estructura de contexto
-   GetXStateFeaturesMask para devolver la máscara de las características de XState establecidas en una estructura de contexto
-   SetXStateFeaturesMask para establecer la máscara de las características de XState establecidas en una estructura de contexto

  


## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   Para obtener información sobre las funciones de XState en el Windows SDK, vea [depurar funciones](../debug/debugging-functions.md).
-   Para obtener información general sobre las instrucciones y capacidades de Intel AVX, consulte [Intel AVX: nuevas fronteras en mejoras de rendimiento y eficiencia energética](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
