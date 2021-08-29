---
title: Principales herramientas y técnicas para crear juegos de Windows más sólidos
description: En este artículo se describen las herramientas y técnicas que puede usar para ayudar a reducir el número de llamadas de soporte técnico que recibe.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecee561149063ba80e47c2b6560441bebf6c851a61187cc9fbbd9e3278e71686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901995"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>Principales herramientas y técnicas para crear juegos de Windows más sólidos

Uno de los costos más no deseados a los que se enfrenta la producción de juegos son las llamadas de soporte técnico. Cada vez que un usuario se pone en contacto con el soporte al cliente, se reducen los beneficios del juego. Aunque algunas llamadas al servicio de atención al cliente no se pueden evitar, otras se pueden eliminar o reducir mediante el empleo de procedimientos de desarrollo recomendados. En este artículo se describen las herramientas y técnicas que puede usar para ayudar a reducir el número de llamadas de soporte técnico que recibe.

Todas las herramientas que se describen aquí son gratuitas y las técnicas son lo suficientemente sencillas como para agregar a la mayoría de los métodos de desarrollo.

Herramientas y técnicas:

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Compatibilidad de aplicaciones de Microsoft Toolkit](#microsoft-application-compatibility-toolkit)
-   [Pruebas de protección de cuentas de usuario](#user-account-protection-testing)
-   [PIXEL para Windows](#pix-for-windows)
-   [Detección de configuración](#configuration-detection)
-   [Habilitar advertencias del compilador completo](#enable-full-compiler-warnings)
-   [Servidor de símbolos de Microsoft](#microsoft-symbol-server)
-   [Informe de errores de Windows](#windows-error-reporting)
-   [Herramientas de optimización del rendimiento](#performance-tuning-tools)
-   [Resumen](#summary)

## <a name="prefast"></a>PREfast

PREfast for Drivers es una herramienta que ofrece Microsoft que analiza las rutas de ejecución en C o C++ compilados para ayudar a encontrar errores en tiempo de ejecución. PREfast funciona trabajando a través de todas las rutas de ejecución en todas las funciones y evaluando cada ruta de acceso para ver si hay problemas. Aunque esta herramienta se usa normalmente para desarrollar controladores y otro código kernel, puede ayudar a los desarrolladores de juegos a ahorrar tiempo mediante la eliminación de algunos errores que son difíciles de encontrar o que el compilador ignora. El uso de PREfast es una excelente manera de reducir la carga de trabajo posterior al lanzamiento y los costos de soporte técnico.

PREfast incluye Visual Studio Team System y como parte de [Windows Driver Kit](https://www.microsoft.com/whdc/devtools/WDK/). Para obtener más información sobre PREfast, vea [PREfast for Drivers](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

Microsoft Application Verifier, o AppVerifier, es una herramienta que puede ayudar a los evaluadores proporcionando varias funciones en una herramienta. AppVerifier se desarrolló para facilitar la prueba de errores de programación comunes. AppVerifier puede comprobar los parámetros que se pasan en las llamadas API, insertar entradas erróneas para comprobar la capacidad de control de errores y registrar los cambios en el registro y el sistema de archivos. AppVerifier también puede detectar saturaciones de búfer en el montón, comprobar que se ha definido correctamente una lista de control de acceso (ACL) y aplicar el uso seguro de las API de sockets.

Aunque no es exhaustivo, AppVerifier puede ser un componente más del cuadro de herramientas de un evaluador para ayudar a un estudio de desarrollo a publicar un producto de calidad y reducir los posibles costos posteriores al lanzamiento.

Para obtener más información sobre Application Verifier, [vea Application Verifier](/previous-versions/ms220948(v=vs.80)) y Uso de Application Verifier dentro del ciclo de vida de desarrollo [de software](/previous-versions/aa480483(v=msdn.10)) en MSDN. Puede descargar Application Verifier descargar [detalles: Application Verifier](https://www.microsoft.com/download/details.aspx?id=20028) en el Centro de descarga de Microsoft.

También hay disponible una herramienta similar para los controladores, Driver Verifier. Para obtener más información, consulte [Uso del comprobador](https://support.microsoft.com/Default.aspx?kbid=244617) de controladores para identificar problemas con Windows controladores para usuarios avanzados en Ayuda y soporte técnico de Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Compatibilidad de aplicaciones de Microsoft Toolkit

Microsoft Application Compatibility Toolkit es un conjunto de herramientas gratuitas que ayudan a los desarrolladores a comprobar rápidamente cómo se realizarán sus versiones en los Service Pack recién publicados para Microsoft Windows. Al estar listos para los nuevos Service Pack, los desarrolladores pueden evitar o estar listos para cualquier problema.

El cuadro de Toolkit compatibilidad de aplicaciones, y más información, se puede encontrar en Windows Application Compatibility (Compatibilidad [de aplicaciones).](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx)

## <a name="user-account-protection-testing"></a>Pruebas de protección de cuentas de usuario

Windows Vista y Windows 7 tienen dos tipos principales de cuentas de usuario: Usuario estándar y Administrador. Las cuentas de usuario estándar son el tipo preferido para todos los usuarios, ya que reducen el riesgo de daños en el sistema por parte de aplicaciones malintencionadas. Dado que el usuario estándar tiene restricciones de acceso, como no poder escribir en la carpeta Archivos de programa o en HKEY \_ LOCAL MACHINE (HKLM) en el Registro, es importante que los juegos se diseñe y se probarán para que funcionen con una cuenta de usuario \_ estándar.

Puede encontrar más información sobre este tema en los artículos [Patching Game Software en Windows XP, Windows Vista y Windows 7](./patching-methods-in-windows-xp-and-vista.md) y Control de cuentas de usuario para desarrolladores de [juegos.](./user-account-control-for-game-developers.md)

## <a name="pix-for-windows"></a>PIXEL para Windows

PIXEL es una herramienta para recopilar y analizar información de rendimiento de una aplicación en ejecución. PIXEL puede recopilar datos estadísticos sobre por qué algunos fotogramas se representan más lentamente que otros y pueden identificar un uso deficiente de la API. TAMBIÉN se puede automatizar LAV para probar la compilación diaria y marcar cambios repentinos en el rendimiento de la aplicación. Mediante el uso de PIXEL en una variedad de configuraciones de hardware, los evaluadores y desarrolladores pueden ayudar a minimizar las llamadas de soporte técnico relacionadas con el rendimiento del juego.

## <a name="configuration-detection"></a>Detección de configuración

Las funcionalidades de dispositivo expuestas por los controladores no siempre son correctas. Una solución es usar un sistema basado en base de datos para la configuración de aplicaciones, como el sistema mostrado en el ejemplo ConfigSystem, que se incluye con el SDK de DirectX. Un modelo de detección similar al sistema del ejemplo puede ayudar a identificar las funcionalidades del dispositivo que están dificultando el rendimiento del juego y, por tanto, reducir el número de llamadas de soporte técnico sobre el rendimiento.

## <a name="enable-full-compiler-warnings"></a>Habilitar advertencias del compilador completo

Es una buena práctica restaurar las advertencias del compilador deshabilitadas por la **\# advertencia pragma** una vez que un proyecto se ha vuelto estable. Los desarrolladores deben intentar eliminar todas las advertencias antes de publicar un producto. Incluso si una advertencia no provoca un bloqueo o un error en el sistema de un desarrollador, podría causar un problema en el sistema de un usuario. Si no se puede eliminar una advertencia, el equipo de prueba debe determinar si la advertencia provocará pocos errores o no en el sistema de un usuario.

## <a name="microsoft-symbol-server"></a>Servidor de símbolos de Microsoft

Microsoft proporciona un servidor accesible desde Internet que proporciona archivos de símbolos para los sistemas operativos Windows Microsoft, así como otros productos de Microsoft. Los símbolos también están disponibles en el servidor para las versiones beta actuales y los candidatos de lanzamiento de Windows productos, así como correcciones de acceso rápido y Service Pack. Puede configurar el depurador para descargar símbolos según sea necesario durante una sesión de depuración, en lugar de descargar archivos de símbolos por separado antes de una sesión de depuración. Los símbolos se descargan en una ubicación de directorio que especifique y el depurador los carga desde allí.

Para obtener más información sobre el servidor de símbolos de Microsoft, vea Herramientas y símbolos de [depuración: Tareas iniciales](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Informe de errores de Windows

Informe de errores de Windows (WER) es un servicio proporcionado por Microsoft para ayudar a los desarrolladores a recopilar información de errores de aplicaciones de forma unificada y organizada. Aunque es completamente voluntaria, los desarrolladores deben aprovechar este servicio para ayudar a determinar qué errores se producen con más frecuencia. El uso de WER puede ayudar con la depuración de problemas comúnmente notificados, lo que ayudará a eliminar las llamadas de soporte técnico para los errores más comunes.

Para obtener más información sobre WER, vea [Análisis de volcado de memoria.](./crash-dump-analysis.md)

## <a name="performance-tuning-tools"></a>Herramientas de optimización del rendimiento

Los desarrolladores pueden usar analizadores de rendimiento para optimizar el rendimiento de su juego. Además de PIXEL, hay una serie de analizadores de rendimiento populares para Windows, como [Intel VTune Analizador de rendimiento](https://software.intel.com/intel-vtune/) y [AMD CodeAnalyst Analizador de rendimiento](https://developer.amd.com/cpu/CodeAnalyst/). Estas herramientas ayudan a identificar cuellos de botella y a decidir cómo mejorar el rendimiento general de una aplicación. Mejorar los cuellos de botella de rendimiento antes de la versión ayudará a reducir los costos posteriores a la versión.

## <a name="summary"></a>Resumen

Todos los implicados en el diseño, el desarrollo y las pruebas deben tener en cuenta cómo afectará su trabajo al costo posterior al lanzamiento de un producto. Mediante el uso de las herramientas y métodos mencionados anteriormente en el proceso de producción, se puede reducir el volumen de llamadas de soporte técnico. Esto, a su vez, aumentará los beneficios al reducir los costos posteriores al lanzamiento del desarrollo de juegos.

 

 