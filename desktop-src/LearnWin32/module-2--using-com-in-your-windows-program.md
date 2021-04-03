---
title: Usar COM en la aplicación de Windows
description: En el módulo 1 de esta serie se ha mostrado cómo crear una ventana y responder a mensajes de ventana, como WM \_ Paint y el cierre de WM \_ . El módulo 2 presenta el modelo de objetos componentes (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791362"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Módulo 2. Usar COM en el programa Windows-Based

En el [módulo 1](your-first-windows-program.md) de esta serie se ha mostrado cómo crear una ventana y responder a mensajes de ventana, como [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) y el [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close). El módulo 2 presenta el modelo de objetos componentes (COM).

COM es una especificación para crear componentes de software reutilizables. Muchas de las características que usará en un programa moderno basado en Windows se basan en COM, como los siguientes:

-   Gráficos (Direct2D)
-   Texto (DirectWrite)
-   Shell de Windows
-   Control Ribbon
-   Animación de IU

(Algunas tecnologías de esta lista usan un subconjunto de COM y, por lo tanto, no son "puras" COM).

COM tiene una reputación por ser difícil de aprender. Y es cierto que escribir un nuevo módulo de software para admitir COM puede ser complicado. Pero si el programa es estrictamente un *consumidor* de com, puede encontrar que com es más fácil de entender de lo esperado.

En este módulo se muestra cómo llamar a las API basadas en COM en el programa. También describe algunas de las razones por las que se basa el diseño de COM. Si entiende por qué COM está diseñado tal cual, puede programar con más eficacia. En la segunda parte del módulo se describen algunos procedimientos recomendados de programación para COM.

COM se presentó en 1993 para admitir la vinculación e incrustación de objetos (OLE) 2,0. A veces, los usuarios piensan que COM y OLE son lo mismo. Esto puede ser otro motivo para la percepción de que COM es difícil de aprender. OLE 2,0 se basa en COM, pero no es necesario conocer OLE para comprender COM.

COM es un *estándar binario*, no un estándar de lenguaje: define la interfaz binaria entre una aplicación y un componente de software. Como estándar binario, COM es independiente del lenguaje, aunque se asigna de forma natural a ciertas construcciones de C++. Este módulo se centrará en tres objetivos principales de COM:

-   Separar la implementación de un objeto de su interfaz.
-   Administrar la duración de un objeto.
-   Detectar las capacidades de un objeto en tiempo de ejecución.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué es una interfaz COM?](what-is-a-com-interface-.md)
-   [Inicializar la biblioteca COM](initializing-the-com-library.md)
-   [Códigos de error en COM](error-codes-in-com.md)
-   [Crear un objeto en COM](creating-an-object-in-com.md)
-   [Ejemplo: el cuadro de diálogo abrir](example--the-open-dialog-box.md)
-   [Administrar la duración de un objeto](managing-the-lifetime-of-an-object.md)
-   [Solicitar un objeto para una interfaz](asking-an-object-for-an-interface.md)
-   [Asignación de memoria en COM](memory-allocation-in-com.md)
-   [Prácticas de codificación COM](com-coding-practices.md)
-   [Control de errores en COM](error-handling-in-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aprender a programar para Windows en C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 