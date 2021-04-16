---
title: Principales herramientas y técnicas para crear juegos de Windows más sólidos
description: En este artículo se describen las herramientas y técnicas que puede usar para reducir el número de llamadas de soporte técnico que recibe.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76b49c228af6a932c453b11e92f612d3419a4af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487994"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>Principales herramientas y técnicas para crear juegos de Windows más sólidos

Uno de los costos más no deseables para la producción de juegos es la compatibilidad con llamadas. Cada vez que un usuario se pone en contacto con el servicio de soporte al cliente, se reduce el beneficio del juego. Aunque algunas llamadas al servicio de soporte al cliente no son imposibles, otras se pueden eliminar o reducir empleando buenas prácticas de desarrollo. En este artículo se describen las herramientas y técnicas que puede usar para reducir el número de llamadas de soporte técnico que recibe.

Todas las herramientas que se describen aquí son gratuitas y las técnicas son lo suficientemente simples para agregarse a la mayoría de los métodos de desarrollo.

Herramientas y técnicas:

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Kit de herramientas de compatibilidad de aplicaciones de Microsoft](#microsoft-application-compatibility-toolkit)
-   [Pruebas de protección de cuentas de usuario](#user-account-protection-testing)
-   [PIX para Windows](#pix-for-windows)
-   [Detección de configuración](#configuration-detection)
-   [Habilitar advertencias completas del compilador](#enable-full-compiler-warnings)
-   [Servidor de símbolos de Microsoft](#microsoft-symbol-server)
-   [Informe de errores de Windows](#windows-error-reporting)
-   [Herramientas de optimización del rendimiento](#performance-tuning-tools)
-   [Resumen](#summary)

## <a name="prefast"></a>PREfast

PREfast para controladores es una herramienta ofrecida por Microsoft que analiza las rutas de acceso de ejecución de C o C++ compiladas para ayudar a encontrar errores en tiempo de ejecución. La función PREfast funciona a través de todas las rutas de ejecución en todas las funciones y la evaluación de cada ruta de acceso. Aunque esta herramienta se usa normalmente para desarrollar controladores y otro código de kernel, puede ayudar a los desarrolladores de juegos a ahorrar tiempo al eliminar algunos errores que son difíciles de encontrar o que el compilador omite. El uso de PREfast es una forma excelente de reducir la carga de trabajo y los costos de soporte técnico posteriores a la versión.

PREfast incluye Visual Studio Team System y como parte del kit de [controladores de Windows](https://www.microsoft.com/whdc/devtools/WDK/). Para obtener más información acerca de PREfast, vea [PREfast para los controladores](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

Microsoft comprobador de aplicaciones, o AppVerifier, es una herramienta que puede ayudar a los evaluadores a proporcionar varias funciones en una sola herramienta. AppVerifier se desarrolló para facilitar la prueba de errores comunes de programación. AppVerifier puede comprobar los parámetros que se pasan en las llamadas API, inyectar entradas erróneas para comprobar la capacidad de control de errores y registrar los cambios en el registro y el sistema de archivos. AppVerifier también puede detectar saturaciones del búfer en el montón, comprobar que se ha definido correctamente una lista de control de acceso (ACL) y aplicar el uso seguro de las API de Sockets.

Aunque no es exhaustivo, AppVerifier puede ser uno de los componentes más del cuadro de herramientas de un evaluador para ayudar a un lanzamiento de Development Studio en un producto de calidad y reducir los posibles costos posteriores a la versión.

Para obtener más información acerca de comprobador de aplicaciones, vea [Comprobador de aplicaciones](/previous-versions/ms220948(v=vs.80)) y [uso de Comprobador de aplicaciones dentro del ciclo de vida de desarrollo de software](/previous-versions/aa480483(v=msdn.10)) en MSDN. Puede descargar comprobador de aplicaciones de detalles de la [descarga: Comprobador de aplicaciones](https://www.microsoft.com/download/details.aspx?id=20028) en el centro de descarga de Microsoft.

También está disponible una herramienta similar para controladores, comprobador de controladores. Para obtener más información, consulte [uso del comprobador de controladores para identificar problemas con los controladores de Windows para usuarios avanzados](https://support.microsoft.com/Default.aspx?kbid=244617) en ayuda y soporte técnico de Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Kit de herramientas de compatibilidad de aplicaciones de Microsoft

El kit de herramientas de compatibilidad de aplicaciones de Microsoft es un conjunto de herramientas gratuitas para ayudar a los desarrolladores a comprobar rápidamente cómo funcionarán sus versiones en los Service Packs recién publicados para Microsoft Windows. Al estar preparado para los nuevos Service Packs, los desarrolladores pueden evitar o estar preparados para cualquier problema.

El kit de herramientas de compatibilidad de aplicaciones y más información se puede encontrar en [compatibilidad de aplicaciones de Windows](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx).

## <a name="user-account-protection-testing"></a>Pruebas de protección de cuentas de usuario

Windows Vista y Windows 7 tienen dos tipos principales de cuentas de usuario: usuario estándar y administrador. Las cuentas de usuario estándar son el tipo preferido para todos los usuarios, ya que reducen el riesgo de daños en el sistema por parte de aplicaciones malintencionadas. Dado que el usuario estándar tiene restricciones de acceso, como no ser capaz de escribir en la carpeta archivos de programa o en el \_ equipo local HKEY \_ (HKLM) del registro, es importante que los juegos se diseñen y prueben para trabajar con una cuenta de usuario estándar.

Puede encontrar más información sobre este tema en los artículos sobre la [revisión de software de juegos en Windows XP, Windows Vista y Windows 7](./patching-methods-in-windows-xp-and-vista.md) y el [control de cuentas de usuario para desarrolladores de juegos](./user-account-control-for-game-developers.md).

## <a name="pix-for-windows"></a>PIX para Windows

PIX es una herramienta para recopilar y analizar información de rendimiento de una aplicación en ejecución. PIX puede recopilar datos estadísticos sobre por qué algunos fotogramas se representan más lentamente que otros y pueden identificar un uso deficiente de la API. PIX también se puede automatizar para probar la compilación diaria y marcar los cambios repentinos en el rendimiento de la aplicación. Al usar PIX en una variedad de configuraciones de hardware, los evaluadores y los desarrolladores pueden ayudar a minimizar las llamadas de soporte técnico relacionadas con el rendimiento de los juegos.

## <a name="configuration-detection"></a>Detección de configuración

Las funcionalidades de dispositivo que exponen los controladores no siempre son correctas. Una solución consiste en usar un sistema controlado por base de datos para la configuración de aplicaciones, como se muestra en el sistema de ejemplo ConfigSystem, que se incluye con el SDK de DirectX. Un modelo de detección similar al del sistema en el ejemplo puede ayudar a identificar las funciones del dispositivo que dificultan el rendimiento del juego y, por lo tanto, reducir el número de llamadas de soporte técnico sobre el rendimiento.

## <a name="enable-full-compiler-warnings"></a>Habilitar advertencias completas del compilador

Es recomendable restaurar las advertencias del compilador que se deshabilitaron mediante **\# pragma warning** una vez que un proyecto se ha vuelto estable. Los desarrolladores deben intentar eliminar todas las advertencias antes de lanzar un producto. Incluso si una advertencia no provoca un bloqueo o un error en el sistema de un desarrollador, podría producirse un problema en el sistema de un usuario. Si no se puede eliminar una advertencia, el equipo de pruebas debe determinar si la advertencia producirá algunos errores o no en el sistema de un usuario.

## <a name="microsoft-symbol-server"></a>Servidor de símbolos de Microsoft

Microsoft proporciona un servidor accesible desde Internet que proporciona archivos de símbolos para los sistemas operativos Microsoft Windows, así como otros productos de Microsoft. También hay símbolos disponibles en el servidor para las versiones beta actuales y versiones candidatas de lanzamiento de productos de Windows, así como revisiones y Service Packs. Puede configurar el depurador para que descargue los símbolos según sea necesario durante una sesión de depuración, en lugar de descargar los archivos de símbolos por separado antes de una sesión de depuración. Los símbolos se descargan en una ubicación de directorio que especifique y el depurador los carga desde allí.

Para obtener más información sobre el servidor de símbolos de Microsoft, vea [herramientas de depuración y símbolos: Introducción](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Informe de errores de Windows

Informe de errores de Windows (WER) es un servicio que proporciona Microsoft para ayudar a los desarrolladores a recopilar información sobre los errores de las aplicaciones de forma unificada y organizada. Aunque es totalmente voluntaria, los desarrolladores deben aprovechar este servicio para ayudar a determinar qué errores se producen con más frecuencia. El uso de WER puede ayudar en la depuración de los problemas más frecuentes, lo que ayuda a eliminar las llamadas de soporte técnico para los errores más de Commons.

Para obtener más información acerca de WER, vea [análisis de volcado](./crash-dump-analysis.md)de memoria.

## <a name="performance-tuning-tools"></a>Herramientas de optimización del rendimiento

Los desarrolladores pueden usar analizadores de rendimiento para ajustar el rendimiento de su juego. Además de PIX, hay una serie de analizadores de rendimiento conocidos para Windows, como el analizador de [rendimiento Intel VTune](https://software.intel.com/intel-vtune/) y el [analizador de rendimiento de AMD CodeAnalyst](https://developer.amd.com/cpu/CodeAnalyst/). Estas herramientas ayudan a identificar cuellos de botella y a decidir cómo mejorar el rendimiento general de una aplicación. La mejora de los cuellos de botella de rendimiento antes del lanzamiento le ayudará a reducir los costes posteriores a la versión.

## <a name="summary"></a>Resumen

Todo el mundo implicado en el diseño, el desarrollo y las pruebas deben tener en cuenta cómo afectará su trabajo al costo posterior a la versión de un producto. Con las herramientas y los métodos mencionados anteriormente en el proceso de producción, se puede reducir el volumen de llamadas de soporte técnico. Esto, a su vez, aumentará los beneficios reduciendo los costes posteriores a la versión del desarrollo de juegos.

 

 