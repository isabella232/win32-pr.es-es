---
title: Introducción a la capa de depuración de Direct2D
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656257"
---
# <a name="direct2d-debug-layer-overview"></a>Introducción a la capa de depuración de Direct2D

El nivel de depuración de Direct2D proporciona mensajes de depuración en tiempo de diseño para que pueda minimizar el error de aplicación en tiempo de ejecución. En esta información general se describen los conceptos básicos del nivel de depuración de Direct2D. Se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D.

Esta información general contiene las siguientes secciones.

-   [¿Qué es el nivel de depuración de Direct2D?](#what-is-the-direct2d-debug-layer)
-   [Instalar la capa de depuración de Direct2D](#installing-the-direct2d-debug-layer)
-   [Habilitar la capa de depuración](#enabling-the-debug-layer)
-   [Niveles de depuración](#debug-levels)
-   [Temas relacionados](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>¿Qué es el nivel de depuración de Direct2D?

La capa de depuración de Direct2D, implementada de forma independiente de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración para que pueda usar con precisión las funciones de Direct2D. Los mensajes de depuración se suelen producir a causa de infracciones del contrato de API, como parámetros no válidos (pueden estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y problemas de rendimiento como el uso de una capa cuando un clip sería suficiente. Para especificar la cantidad de información de la que se realiza el seguimiento por la capa de depuración, puede especificar uno de los tres niveles de depuración: información, ADVERTENCIA y error. y un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.

## <a name="installing-the-direct2d-debug-layer"></a>Instalar la capa de depuración de Direct2D

Para obtener instrucciones sobre cómo instalar la capa de depuración, vea [instalar la capa de depuración de Direct2D](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Habilitar la capa de depuración

Para habilitar la capa de depuración en la aplicación, especifique un valor de [**\_ \_ nivel de depuración de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) distinto de **D2D1 \_ Debug \_ LEVEL \_ None** al crear un generador con la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .

> [!Note]  
> Si la capa de depuración de Direct2D está habilitada, el efecto de administración del color de Direct2D (CLSID \_ D2D1ColorManagement) puede producir una infracción de acceso al establecer un contexto de color. La solución consiste en deshabilitar la capa de depuración cuando se usa el efecto administración del color

 

Habilitar la capa de depuración para un generador también habilita la información de depuración para cualquier objeto creado por ese generador.

En el ejemplo siguiente se habilita la capa de depuración para un generador cuando la aplicación se compila para la configuración de compilación de depuración.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> Si no se especifican opciones de fábrica o se especifica un nivel de depuración "none", no se invoca la capa de depuración. La capa de depuración nunca debe estar activa en la versión de lanzamiento de una aplicación.

 

En la sección siguiente se describen los diferentes niveles de depuración definidos por la enumeración de [**\_ \_ nivel de depuración D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .

## <a name="debug-levels"></a>Niveles de depuración

La enumeración de [**\_ \_ nivel**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) de depuración D2D1 especifica tres niveles de depuración: error de depuración de D2D1 \_ \_ \_ (error), D2D1 de advertencia de nivel de depuración \_ \_ \_ (ADVERTENCIA) e \_ información de nivel de depuración D2D1 \_ \_ (información) Estos niveles se interpretan de la siguiente manera:

-   **Error:** Direct2D envía mensajes de error graves a la capa de depuración. Por ejemplo, si se interrumpe una restricción de subproceso, se producirá un error grave.

-   **ADVERTENCIA:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda tratar cualquiera de estos mensajes.

-   **Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración. Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.

El valor de \_ nivel de depuración D2D1 \_ \_ ninguno (ninguno) indica que Direct2D no proporciona ningún resultado de depuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar mensajes](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




