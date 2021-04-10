---
title: Instrucciones generales de portabilidad
description: La migración de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la migración de aplicaciones de 16 bits a Windows de 32 bits. Sin embargo, el cambio se realizará de forma más fluida con cierta planeación cuidadosa. A continuación se muestran algunas directrices generales.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- trasladar aplicaciones de 32 bits a la programación de Windows de Windows 64 de 64 bits
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, directrices de migración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104279732"
---
# <a name="general-porting-guidelines"></a>Instrucciones generales de portabilidad

La migración de aplicaciones de 32 bits a Microsoft Windows de 64 bits será más fácil que la migración de aplicaciones de 16 bits a Windows de 32 bits. Sin embargo, el cambio se realizará de forma más fluida con cierta planeación cuidadosa. A continuación se muestran algunas directrices generales.

## <a name="planning"></a>Planificación

-   Determinar la magnitud del esfuerzo necesario para el puerto. Mida la cantidad de trabajo que implica la identificación de los siguientes elementos:
    -   Problema 32: código de bit. Compile el código de 32 bits con el compilador de 64 bits y examine la extensión de los errores y las advertencias.
    -   Componentes compartidos o dependencias. Determine qué componentes de la aplicación se originan en otros equipos y si esos equipos planean desarrollar versiones de 64 bits de su código.
    -   Código de ensamblado o heredado. las aplicaciones basadas en Windows de 16 bits no se ejecutan en Windows de 64 bits y se deben volver a escribir. Aunque el código de ensamblado x86 se ejecuta en WOW64, puede que desee volver a escribir este código para aprovechar la velocidad de la arquitectura Intel Itanium.
-   Porte toda la aplicación, no solo partes de ella.

    Aunque es posible migrar partes de una aplicación o limitar el código a 2G con/LARGEADDRESSAWARE: NO, esta estrategia negocia la ganancia a corto plazo para el dolor a largo plazo.

    > [!Note]  
    > /LARGEADDRESSAWARE: NO se omite para un binario ARM64.

     

-   Busque sustitutos para las tecnologías que no se van a migrar.

    Algunas tecnologías, como DAO (objeto de acceso a datos) y el motor de base de datos de jet red, no se trasladarán a Windows de 64 bits.

-   Trate la versión de 64 bits como una versión de producto independiente.

    Aunque el producto de 64 bits puede compartir el mismo código base que el de 32 bits, necesita pruebas adicionales y puede tener otras consideraciones de la versión.

## <a name="development"></a>Desarrollo

-   Comience a desarrollar código compatible ahora.

    Los desarrolladores pueden empezar a escribir código compatible con los archivos de encabezado de Windows más recientes y los nuevos tipos de datos sin efectos negativos en el desarrollo de productos de 32 bits. Para obtener más información, consulte [preparación para Windows de 64 bits](getting-ready-for-64-bit-windows.md).

-   Asegúrese de que el código se puede compilar para Windows de 32 y 64 bits.

    El nuevo modelo de datos se diseñó para permitir la creación de aplicaciones de 32 y 64 bits a partir de una única base de código con pocas modificaciones. Los equipos de desarrollo de SQL Server y Windows están desarrollando versiones de 32 y 64 bits de sus productos a partir de la misma base de código.

-   Use las nuevas características de optimización del compilador para obtener el mejor rendimiento.

    La optimización del código para procesadores Intel Itanium es más importante que para x86. El compilador supone muchas de las funciones de optimización que el microprocesador ha controlado previamente. Puede maximizar el rendimiento de una aplicación de 64 bits con dos nuevas características de optimización del compilador: *optimización guiada por perfiles* y *optimización completa del programa*. Ambas características generan tiempos de compilación más prolongados y requieren el desarrollo temprano de Buenos escenarios de prueba.

    La *optimización guiada por perfiles* implica un proceso de compilación de dos pasos. Durante la primera compilación, el código se instrumenta para capturar el comportamiento de ejecución. Esta información se utiliza durante la segunda compilación para guiar todas las características de optimización.

    La *optimización de todo el programa* analiza el código en todos los archivos de aplicación, no solo en uno único. Este enfoque aumenta el rendimiento de varias maneras, como una mejor inserción, así como el análisis de efectos secundarios mejorado y las convenciones de llamada personalizadas.

## <a name="testing"></a>Prueba

-   Determine si va a probar el código de 64 o 32 bits que se ejecuta en WOW64.

    Algunas aplicaciones incluyen código nativo de 64 bits y código de 32 bits que se ejecuta en WOW64. Investigue esto estrechamente durante el desarrollo de un plan de pruebas y decida si las herramientas de pruebas deben ser de 64 bits, de 32 bits o de combinación. A menudo, necesitará probar las versiones de 64 y 32 bits de su aplicación en Windows de 64 bits.

-   Pruebe los componentes de 32 bits usados con frecuencia.

    En primer lugar, vuelva a compilar el código en 64 bits y pruebe. En segundo lugar, solucione los problemas, vuelva a compilar en 32 bits y, a continuación, pruebe. En tercer lugar, vuelva a compilar a 64 bits y test.

-   Probar componentes COM y RPC.

    Asegúrese de que los componentes COM y RPC de 32 y 64 bits se comunican correctamente. También es posible que tenga que probar las comunicaciones con componentes de 16 bits a través de una red.

-   Pruebe la versión de 32 bits en Windows de 64 bits.

    Los clientes pueden seguir usando aplicaciones de 32 bits en Windows de 64 bits, donde los problemas de rendimiento y de memoria no son consideraciones importantes.

-   Pruebe diferentes configuraciones de memoria.

    Al agregar grandes cantidades de memoria en el servidor, a veces se exponen problemas no detectados anteriormente en la aplicación o en el sistema operativo.

 

 




