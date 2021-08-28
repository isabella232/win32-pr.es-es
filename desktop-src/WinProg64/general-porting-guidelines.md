---
title: Directrices generales de porte
description: La porción de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la porción de aplicaciones de 16 bits a aplicaciones de 32 Windows. Sin embargo, el traslado se realizará más sin problemas con una planeación cuidadosa. Estas son algunas directrices generales.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Porción de aplicaciones de 32 bits a programación de 64 Windows de 64 Windows bits
- Guía de programación de 64 Windows de programación de 64 Windows programación, directrices de porte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a586318ecc6ec8852077052cbcff41bffacff6c35c36d23de4b020ce19f12af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680245"
---
# <a name="general-porting-guidelines"></a>Directrices generales de porte

La porción de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la porción de aplicaciones de 16 bits a aplicaciones de 32 Windows. Sin embargo, el traslado se realizará más sin problemas con una planeación cuidadosa. Estas son algunas directrices generales.

## <a name="planning"></a>Planificación

-   Determine la magnitud del esfuerzo necesario para el puerto. Mida la cantidad de trabajo implicado mediante la identificación de los siguientes elementos:
    -   Código de 32 bits del problema. Compile el código de 32 bits con el compilador de 64 bits y examine la extensión de los errores y advertencias.
    -   Componentes o dependencias compartidos. Determine qué componentes de la aplicación se originan en otros equipos y si planean desarrollar versiones de 64 bits de su código.
    -   Código heredado o de ensamblado. Las aplicaciones basadas Windows de 16 bits no se ejecutan en aplicaciones de 64 Windows y se deben volver a escribir. Aunque el código de ensamblado x86 se ejecuta en WOW64, es posible que quiera volver a escribir este código para aprovechar la velocidad de la arquitectura Intel Itanium.
-   Porte toda la aplicación, no solo partes de ella.

    Aunque es posible portabilidad de fragmentos de una aplicación o limitar el código a 2G con /LARGEADDRESSAWARE:NO, esta estrategia negocia la ganancia a corto plazo por problemas a largo plazo.

    > [!Note]  
    > /LARGEADDRESSAWARE:NO se omite para un binario ARM64.

     

-   Busque sustitutos de tecnologías que no se van a porte.

    Algunas tecnologías, como DAO (objeto de acceso a datos) y el motor de base de datos Jet Red, no se portarán a archivos de 64 Windows.

-   Trate la versión de 64 bits como una versión de producto independiente.

    Aunque el producto de 64 bits puede compartir la misma base de código que el de 32 bits, necesita pruebas adicionales y puede tener otras consideraciones de versión.

## <a name="development"></a>Desarrollo

-   Comience a desarrollar código compatible ahora.

    Los desarrolladores pueden empezar a escribir código compatible con los archivos de encabezado de Windows y los nuevos tipos de datos sin efectos negativos en el desarrollo de productos de 32 bits. Para obtener más información, vea [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

-   Asegúrese de que el código se puede compilar para archivos de 32 y 64 Windows.

    El nuevo modelo de datos se diseñó para permitir que las aplicaciones de 32 y 64 bits se crearon a partir de una base de código única con pocas modificaciones. Los SQL Server y Windows desarrollo están desarrollando versiones de 32 y 64 bits de sus productos desde la misma base de código.

-   Use las nuevas características de optimización del compilador para obtener el mejor rendimiento.

    La optimización de código para procesadores Intel Itanium es más importante que para x86. El compilador presupone muchas de las funciones de optimización previamente controladas por el microprocesador. Puede maximizar el rendimiento de una aplicación de 64 bits mediante dos nuevas características de optimización del *compilador:* Optimización guiada por perfiles y Optimización *de todo el programa*. Ambas características tienen como resultado tiempos de compilación más largos y requieren el desarrollo temprano de buenos escenarios de prueba.

    *La optimización guiada por* perfiles implica un proceso de compilación en dos pasos. Durante la primera compilación, el código se instrumenta para capturar el comportamiento de ejecución. Esta información se usa durante la segunda compilación para guiar todas las características de optimización.

    *Optimización de todo* el programa analiza el código en todos los archivos de aplicación, no solo uno. Este enfoque aumenta el rendimiento de varias maneras, incluida una mejor inclusión, así como el análisis de efectos secundarios mejorados y las convenciones de llamada personalizadas.

## <a name="testing"></a>Prueba

-   Determine si probará código de 64 o 32 bits que se ejecuta en WOW64.

    Algunas aplicaciones incluyen código nativo de 64 bits y código de 32 bits que se ejecuta en WOW64. Investigue esto de cerca al desarrollar un plan de prueba y decida si las herramientas de prueba deben ser de 64 bits, 32 bits o una combinación. A menudo tendrá que probar las versiones de 64 y 32 bits de la aplicación en versiones de 64 Windows.

-   Pruebe los componentes de 32 bits usados con frecuencia.

    En primer lugar, vuelva a compilar el código a 64 bits y pruebe. En segundo lugar, corrija los problemas, vuelva a compilar en 32 bits y, a continuación, pruebe. En tercer lugar, vuelva a compilar a 64 bits y pruebe.

-   Pruebe los componentes COM y RPC.

    Asegúrese de que los componentes COM y RPC de 32 y 64 bits se comunican correctamente. Es posible que también tenga que probar las comunicaciones con componentes de 16 bits a través de una red.

-   Pruebe la versión de 32 bits en versiones de 64 Windows.

    Los clientes pueden seguir usando aplicaciones de 32 bits en aplicaciones de 64 Windows donde los problemas de rendimiento y memoria no son consideraciones importantes.

-   Pruebe diferentes configuraciones de memoria.

    La adición de grandes cantidades de memoria en el servidor a veces expone problemas que anteriormente no se han pasado desapercibieron en la aplicación o en el sistema operativo.

 

 




