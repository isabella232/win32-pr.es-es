---
title: Introducción a la capa de depuración de Direct2D
description: Introducción a la capa de depuración de Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad960c50cd125ec8c335d836949457bb05ef65aba4b2edaff1dfbbd3a9cf6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087775"
---
# <a name="direct2d-debug-layer-overview"></a>Introducción a la capa de depuración de Direct2D

La capa de depuración de Direct2D proporciona mensajes de depuración en tiempo de diseño para minimizar los errores de la aplicación en tiempo de ejecución. En esta introducción se describen los conceptos básicos de la capa de depuración de Direct2D. Se supone que está familiarizado con la creación de aplicaciones básicas de Direct2D.

Esta información general contiene las secciones siguientes.

-   [¿Qué es la capa de depuración de Direct2D?](#what-is-the-direct2d-debug-layer)
-   [Instalación de la capa de depuración de Direct2D](#installing-the-direct2d-debug-layer)
-   [Habilitación de la capa de depuración](#enabling-the-debug-layer)
-   [Niveles de depuración](#debug-levels)
-   [Temas relacionados](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>¿Qué es la capa de depuración de Direct2D?

La capa de depuración de Direct2D, implementada por separado de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración para permitirle usar con precisión las funciones de Direct2D. Los mensajes de depuración suelen ser el resultado de infracciones del contrato de API, como parámetros no válidos (podrían estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y problemas de rendimiento, como el uso de una capa cuando un clip sería suficiente. Para especificar la cantidad de información que se sigue en la capa de depuración, puede especificar uno de los tres niveles de depuración: información, advertencia y error. y un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.

## <a name="installing-the-direct2d-debug-layer"></a>Instalación de la capa de depuración de Direct2D

Para obtener instrucciones sobre cómo instalar la capa de depuración, consulte [Instalación de la capa de depuración de Direct2D.](installing-the-direct2d-debug-layer.md)

## <a name="enabling-the-debug-layer"></a>Habilitación de la capa de depuración

Para habilitar la capa de depuración en la aplicación, especifique un valor [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) distinto de **D2D1 \_ DEBUG LEVEL \_ \_ NONE** al crear un generador con la función [**D2D1CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)

> [!Note]  
> Si la capa de depuración de Direct2D está habilitada, el efecto de administración de colores de Direct2D (CLSID D2D1ColorManagement) puede provocar una infracción de acceso al establecer un contexto \_ de color. La solución alternativa consiste en deshabilitar la capa de depuración cuando se usa el efecto de administración de colores.

 

La habilitación de la capa de depuración para un generador también habilita la información de depuración para cualquier objeto creado por ese generador.

En el ejemplo siguiente se habilita la capa de depuración de un generador cuando la aplicación se compila para la configuración de compilación debug.


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
> Si no se especifica ninguna opción de fábrica o se especifica un nivel de depuración de "none", no se invoca la capa de depuración. La capa de depuración nunca debe estar activa en la versión de lanzamiento de una aplicación.

 

En la sección siguiente se describen los distintos niveles de depuración definidos por la [**enumeración D2D1 \_ DEBUG \_ LEVEL.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)

## <a name="debug-levels"></a>Niveles de depuración

La enumeración [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) especifica tres niveles de depuración: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (error), D2D1 \_ DEBUG LEVEL WARNING (advertencia) e \_ \_ D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (información). Estos niveles se interpretan de la siguiente manera:

-   **Error:** Direct2D envía mensajes de error graves a la capa de depuración. Por ejemplo, la separación de una restricción de subprocesos generará un error grave.

-   **Advertencia:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda abordar cualquiera de estos mensajes.

-   **Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración. Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.

El valor D2D1 DEBUG LEVEL NONE (none) indica que \_ \_ \_ Direct2D no proporciona ninguna salida de depuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar mensajes](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




