---
title: Uso de COM en la Windows aplicación
description: El módulo 1 de esta serie mostró cómo crear una ventana y responder a mensajes de ventana como WM \_ PAINT y WM \_ CLOSE. El módulo 2 presenta el modelo de objetos componentes (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2180d47bd0dd12c0184a2f9241ec5656c7fe711150e1d5163ca2fec9e0b28fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068035"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Módulo 2. Uso de COM en el Windows-Based programa

[El módulo 1](your-first-windows-program.md) de esta serie mostró cómo crear una ventana y responder a mensajes de ventana como [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) y [**WM \_ CLOSE.**](/windows/desktop/winmsg/wm-close) El módulo 2 presenta el modelo de objetos componentes (COM).

COM es una especificación para crear componentes de software reutilizables. Muchas de las características que usará en un programa moderno basado en Windows se basan en COM, como las siguientes:

-   Gráficos (Direct2D)
-   Texto (DirectWrite)
-   Shell de Windows
-   Control de cinta de opciones
-   Animación de la interfaz de usuario

(Algunas tecnologías de esta lista usan un subconjunto de COM y, por lo tanto, no son COM "puros").

COM tiene una reputación de ser difícil de aprender. Y es cierto que escribir un nuevo módulo de software para admitir COM puede ser complicado. Pero si el programa es estrictamente *un consumidor* de COM, es posible que encuentre que COM es más fácil de entender de lo esperado.

En este módulo se muestra cómo llamar a las API basadas en COM en el programa. También se describen algunos de los razonamientos que hay detrás del diseño de COM. Si comprende por qué COM está diseñado tal cual, puede programar con él de forma más eficaz. En la segunda parte del módulo se describen algunas prácticas de programación recomendadas para COM.

COM se introdujo en 1993 para admitir la vinculación e inserción de objetos (OLE) 2.0. A veces, los usuarios creen que COM y OLE son lo mismo. Este puede ser otro motivo para la percepción de que COM es difícil de aprender. OLE 2.0 se basa en COM, pero no es necesario conocer OLE para entender COM.

COM es un *estándar binario,* no un estándar de lenguaje: define la interfaz binaria entre una aplicación y un componente de software. Como estándar binario, COM es neutro en el lenguaje, aunque se asigna de forma natural a determinadas construcciones de C++. Este módulo se centrará en tres objetivos principales de COM:

-   Separación de la implementación de un objeto de su interfaz.
-   Administrar la duración de un objeto.
-   Detección de las funcionalidades de un objeto en tiempo de ejecución.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué es una interfaz COM?](what-is-a-com-interface-.md)
-   [Inicialización de la biblioteca COM](initializing-the-com-library.md)
-   [Códigos de error en COM](error-codes-in-com.md)
-   [Crear un objeto en COM](creating-an-object-in-com.md)
-   [Ejemplo: Cuadro de diálogo Abrir](example--the-open-dialog-box.md)
-   [Administrar la duración de un objeto](managing-the-lifetime-of-an-object.md)
-   [Pedir un objeto para una interfaz](asking-an-object-for-an-interface.md)
-   [Asignación de memoria en COM](memory-allocation-in-com.md)
-   [Prácticas de codificación COM](com-coding-practices.md)
-   [Control de errores en COM](error-handling-in-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aprender a programar para Windows en C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 