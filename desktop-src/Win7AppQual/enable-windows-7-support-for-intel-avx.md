---
description: Habilitación Windows 7 compatibilidad con Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitación Windows 7 compatibilidad con Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30469d0218f5da2c9f6df2b4f5637edffe09153ebad721f48b47401ecb1f3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329819"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Habilitación Windows 7 compatibilidad con Intel AVX

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows 7 SP1  
**Servidores:** Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Intel<sup>?</sup> Advanced Vector Extensions (AVX)<sup>?</sup> es una extensión de vector de punto flotante SIMD de 256 bits de la arquitectura Intel. Incluye extensiones para conjuntos de instrucciones y registros.

Microsoft ha desarrollado algunas mejoras de API, como las funciones XState, que permiten a las aplicaciones acceder a la información y el estado de las características extendidas del procesador, incluido AVX, y manipularlos.

## <a name="usage-scenarios"></a>Escenarios de uso

Hay tres niveles generales de posible impacto.

**Nivel 1:** Las aplicaciones que no usan directamente Intel AVX no verán ningún impacto en su funcionalidad, incluso si llaman a bibliotecas o usan compiladores que usan indirectamente o generan extensiones AVX de Intel. Esto representa con diferencia la mayoría de las aplicaciones.

**Nivel 2:** Las aplicaciones avanzadas que usan explícitamente el conjunto de instrucciones avx de Intel podrán acceder al contenido del registro de AVX y cambiarlo cuando se produce una excepción de hardware. Un número muy pequeño de aplicaciones entraría en esta categoría, ya que implica un conocimiento profundo del flujo de instrucciones que se ejecuta en el momento de la excepción, como las aplicaciones con secciones escritas en lenguaje de ensamblado o las que generan código de máquina en tiempo de ejecución (por ejemplo, tiempos de ejecución de código administrado con compilación Just-In-Time).

**Nivel 3:** Las aplicaciones del depurador podrán acceder y manipular el estado de AVX en la aplicación que se está depurando.

## <a name="how-to-leverage-feature-capabilities"></a>Cómo aprovechar las funcionalidades de características

**Nivel 1:** No es necesario realizar ninguna acción para que las aplicaciones usen Intel AVX.

**Nivel 2:** Las aplicaciones de esta categoría tienen la opción de acceder y manipular el estado de AVX en el momento de la excepción desde dentro de sus filtros de excepción. Después de obtener el contexto del procesador base a través de GetExceptionInformation, los filtros deben:

 **1. Compruebe** el valor de la **marca CONTEXT \_ XSTATE.** Esta marca indica la presencia de al menos una característica XState en el contexto.  
**2.** Si este es el caso, llame a **GetXStateFeaturesMask** y pruebe el valor de la marca **\_ AVX XSTATE** en la máscara devuelta. Esto indica la presencia del estado AVX en el contexto.  
**3.** Llame **a LocateXStateFeature para** recuperar la ubicación real donde se almacena el estado avx.  

**Nivel 3:** No es necesario actualizar las aplicaciones de depurador existentes a menos que deseen acceder a los registros avx de Intel:

**1.** Para determinar si AVX está habilitado, el depurador debe usar:

-   GetEnabledXStateFeatures para obtener una máscara de características XState habilitadas en procesadores x86 o x64 para determinar qué características están presentes y habilitadas en el sistema antes de usar una característica de procesador XState o intentar manipular contextos XState

  
**2.** Si AVX está presente y desea recuperar y manipular el estado avx de la aplicación que se está depurando (por ejemplo, GetThreadContext y SetThreadContext), el depurador debe usar:

-   Función InitializeContext para inicializar una estructura de contexto dentro de un búfer con el tamaño y la alineación necesarios
-   Función CopyContext para copiar una estructura de contexto de origen (incluido cualquier XState) en una estructura de contexto de destino inicializada

  
**3.** Para probar, establecer y localizar el estado de AVX dentro de un contexto de procesador, el depurador debe usar:

-   LocateXStateFeature para recuperar un puntero al estado del procesador de una característica XState individual dentro de una estructura de contexto
-   GetXStateFeaturesMask para devolver la máscara de las características XState establecidas dentro de una estructura de contexto
-   SetXStateFeaturesMask para establecer la máscara de características XState establecida en una estructura de contexto

  


## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   Para obtener información sobre las funciones XState en el SDK Windows, vea [Funciones de depuración](../debug/debugging-functions.md).
-   Para obtener información general sobre las instrucciones y funcionalidades de Intel AVX, consulte [Intel AVX: Nuevas](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/)fronteras en mejoras de rendimiento y eficiencia energética.

 

 
