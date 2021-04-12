---
title: Instalación y mantenimiento de juegos
description: En este artículo se describe un conjunto de prácticas recomendadas que pueden ayudar a reducir la frustración de los usuarios sobre el tiempo necesario para instalar un juego, evitar llamadas innecesarias de soporte técnico y permitir que los usuarios empiecen a reproducir el juego lo más rápido y sin problemas posible.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de171fd76654eb3b6edb8818ec073c4ef5ba8ca4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359387"
---
# <a name="installation-and-maintenance-of-games"></a>Instalación y mantenimiento de juegos

En este artículo se describe un conjunto de prácticas recomendadas que pueden ayudar a reducir la frustración de los usuarios sobre el tiempo necesario para instalar un juego, evitar llamadas innecesarias de soporte técnico y permitir que los usuarios empiecen a reproducir el juego lo más rápido y sin problemas posible.

-   [Instalación inicial](#initial-installation)
    -   [Simplificación de la interfaz de usuario de instalación](#streamlining-the-installation-ui)
    -   [Reducir el tiempo necesario para la instalación](#reducing-the-time-required-for-installation)
    -   [Instalación mínima](#minimal-installation)
    -   [Instalación a petición](#install-on-demand)
-   [Juego posterior a la instalación](#post-installation-game-play)
    -   [Ejecuta](#autorun)
    -   [Convertir una instalación a petición en una instalación completa](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Mantenimiento de software y contenido de juegos](#maintenance-of-game-software-and-content)
    -   [Buscar actualizaciones automáticamente](#checking-for-updates-automatically)
    -   [Descargar revisiones automáticamente](#downloading-patches-automatically)
-   [Otros recursos](#other-resources)
-   [Temas relacionados](#related-topics)

## <a name="initial-installation"></a>Instalación inicial

Los usuarios compran juegos porque están jugando, no porque disfrutan de instalarlos. La instalación de un juego debe ser tan rápida, sencilla y tan fácil como sea posible para el usuario final. Idealmente, los usuarios finales no deberían ver incluso una interfaz de usuario de instalación; deberían ser capaces de quitar el disco del juego en la bandeja y comenzar a reproducir.

### <a name="streamlining-the-installation-ui"></a>Simplificación de la interfaz de usuario de instalación

Los aspectos comunes de las IUs de instalación de juegos existentes interfieren con la experiencia deseada del usuario final:

-   Preguntas innecesarias al usuario.

    Por ejemplo, muchos juegos preguntan si el usuario desea instalar DirectX. Si el juego requiere que se ejecute Microsoft DirectX y ya no está instalada la versión correcta de DirectX, el juego solo debe instalar DirectX.

-   Preguntar a los usuarios que la mayoría de los usuarios responderán de la misma manera.

    Para los usuarios típicos, la configuración predeterminada de la ruta de instalación, la ubicación del menú Inicio, etc., está bien. Ofrezca opciones avanzadas a los usuarios que deseen cambiar esta configuración.

La interfaz de usuario de instalación debe estar diseñada para permitir que el usuario típico empiece a reproducir el juego lo antes posible. Si la ejecución automática está habilitada en el equipo del usuario, que es el valor predeterminado, el programa de instalación debe suponer que el usuario desea jugar lo antes posible, omitiendo las preguntas innecesarias. El programa de instalación programa[instalar a petición](#install-on-demand)m debe empezar a instalar el juego en la ruta de instalación predeterminada, preferiblemente mediante una configuración como la que se describe en. Es adecuado dar a los usuarios una oportunidad para cambiar la configuración de la instalación antes de iniciar la instalación automáticamente. Sin embargo, esto se debe hacer solicitando al usuario que presione una tecla para las opciones de configuración avanzadas y, a continuación, proseguir automáticamente con las opciones predeterminadas si el usuario no alcanza esa clave en un plazo de cinco a diez segundos.

Si la ejecución automática no está habilitada en el equipo del usuario, el programa de instalación debe suponer que el usuario no desea que el programa de instalación empiece a instalar el juego automáticamente. Si el programa de instalación se inicia por algún otro medio que no sea AutoRun, debe iniciar la interfaz de usuario de configuración avanzada.

### <a name="reducing-the-time-required-for-installation"></a>Reducir el tiempo necesario para la instalación

La mayoría de los juegos de Microsoft Windows llevan hoy desde cinco minutos hasta la media hora para finalizar el proceso de instalación. Por el contrario, la mayoría de los juegos de la consola no tardan más de treinta segundos en el momento en que el usuario inserta el CD del juego en el momento en que el usuario puede jugar. Esta diferencia se debe al hecho de que la mayoría de los juegos de Windows están diseñados para ejecutarse la mayor parte del contenido del disco duro del equipo, si no todos. las consolas de, que carecen de un lugar para almacenar de forma permanente grandes cantidades de contenido, requieren que el contenido se ejecute desde los medios de origen. Al cargar el contenido de la unidad de disco duro local, se agilizan los tiempos de carga del juego, el inconveniente es que todo el contenido debe copiarse desde el medio de origen en el disco duro en algún momento. La mayoría de los juegos de Windows elige copiar todo el contenido en la unidad de disco duro a la vez, como parte de un proceso de instalación. Esto distrae de la experiencia inicial del usuario con el juego al hacer que el usuario vea una barra de progreso durante varios minutos antes de poder jugar.

Hay dos enfoques que se pueden usar para minimizar el tiempo empleado en la instalación inicial del juego: [instalación mínima](#minimal-installation) e instalación [a petición](#install-on-demand).

### <a name="minimal-installation"></a>Instalación mínima

En un escenario de instalación mínima, el juego solo instala un conjunto mínimo de contenido en el disco duro. Normalmente, esto solo consta de los archivos ejecutables y dll del juego. Se tiene acceso al resto del contenido directamente desde los medios de origen. Esto reduce drásticamente el tiempo necesario para instalar, ya que el ejecutable de un juego rara vez es mayor que 10-20 MB. El inconveniente es que el juego tarda más tiempo en cargar contenido durante el juego, ya que debe cargarlo desde el medio de origen más lento.

Para crear una configuración de instalación mínima en una instalación basada en Windows Installer:

-   Agrupe todos los componentes que se van a instalar en el disco duro en una característica marcada para instalarse localmente.

    Esta característica se conoce como la característica de "arranque".

-   Agrupe todos los componentes que se van a ejecutar desde los medios de origen en una característica marcada como "ejecutar desde el origen".
-   Al abrir un archivo que podría estar en el medio de origen, use la función [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar la ruta de acceso al archivo, en lugar de codificar de forma rígida la ruta de acceso.

    Al hacerlo se asegura de que el archivo se puede encontrar incluso si cambia la letra de unidad de la unidad de CD/DVD del usuario.

-   Comprimir el contenido que permanece en el CD o DVD.

    La cantidad de tiempo de CPU que se emplea en descomprimir el contenido se oculta normalmente por la velocidad de transferencia lenta de los datos de la unidad de CD/DVD.

-   Agrupe el contenido en archivos grandes y contiguos y acceda a ellos en orden secuencial.

    Los tiempos de búsqueda de las unidades de CD/DVD se Abysmal en comparación con los de las unidades de disco duro, y la mayoría de las unidades de CD/DVD no alcanzan las tasas de transferencia máxima a menos que lean un archivo contiguo y grande.

-   Diseñe el contenido en el CD o DVD en el orden en el que es probable que se tenga acceso a él.

    Los tiempos de búsqueda se reducen considerablemente cuando se tiene acceso a los archivos en el mismo orden que su diseño en disco.

### <a name="install-on-demand"></a>Instalación a petición

En un escenario de instalación a petición, como en el caso de la instalación mínima, el juego primero instala en la unidad de disco duro los archivos necesarios para iniciar el juego. Sin embargo, en lugar de tener acceso al resto del contenido desde el medio de origen cada vez que se necesita, el juego instala realmente cada fragmento de contenido en la unidad de disco duro tal y como se necesita por primera vez y, a continuación, accede a ella desde el disco duro local en cada uso posterior. El tiempo necesario para la instalación inicial es tan pequeño como en el caso de una instalación mínima, pero después de la primera vez que se tiene acceso a cada elemento de contenido, los tiempos de carga mejoran.

Para crear una configuración de instalación a petición en una instalación basada en Windows Installer:

-   Agrupe todos los componentes que se instalarán inicialmente en el disco duro en una característica marcada para instalarse localmente.

    Tenga en cuenta que esto es idéntico a la característica bootstrap para una instalación mínima.

-   Agrupe el contenido restante en varias características en función de los componentes que puedan usarse juntos.

    Por ejemplo, en un juego basado en niveles, agrupe todo el contenido que se usa en un nivel determinado en una característica. Tenga en cuenta que Windows Installer permite que varias características compartan un componente, por lo que si tiene contenido que se usa en varios niveles, puede agregar ese contenido a las características de todos los niveles necesarios sin replicar el contenido. Todas estas características se deben marcar como "anunciadas", lo que significa que no se instalarán inicialmente, pero se pueden instalar más adelante según sea necesario.

-   Cuando se necesite un archivo, compruebe primero si el archivo ya está instalado mediante la función [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea).

    Si aún no está instalado (es decir, su estado es INSTALLSTATE \_ anunciado), llame a la función [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar la característica de forma local. Al abrir el archivo una vez instalado, llame a [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar la ruta de acceso al archivo. Aunque no es estrictamente necesario para este escenario (dado que el contenido siempre se instalará en el disco duro antes de que se utilice), esto facilita la compatibilidad con la instalación mínima además de la instalación a petición.

-   Si es posible, prevea el contenido que es probable que se necesite pronto e instálelo en segundo plano durante el tiempo de inactividad.

    La instalación en segundo plano es más adecuada cuando el juego está en un punto que no necesita todos los últimos onzas de rendimiento del equipo; por ejemplo, al mostrar una película introductoria, una escena corta, un menú, etc.

-   Cree una opción en el menú de opciones del juego para forzar la instalación de todo el contenido restante.

    Para implementarlo, cree una característica que sea un elemento primario de todas las características de instalación a petición y, a continuación, llame a [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar esta característica principal de forma local. Esto hará que las subcaracterísticas se instalen también localmente.

-   La distribución del contenido debe ser similar a la de una instalación mínima, excepto en que el contenido se debe agrupar solo con otro contenido que probablemente sea necesario al mismo tiempo (por ejemplo, todo el contenido de un nivel debe ser conjunto).

## <a name="post-installation-game-play"></a>Game-Play posterior a la instalación

### <a name="autorun"></a>Ejecuta

Para reproducir un juego que ya está instalado, el usuario solo debe quitar el disco de instalación en la bandeja de la unidad. Lo primero que debe hacer el ejecutable de ejecución automática en el disco es comprobar si el juego ya está instalado y, si es así, iniciar el juego. Suponiendo que el juego se instaló mediante una instalación basada en Windows Installer, la comprobación para determinar si el juego está instalado puede realizarse con una sola llamada a la función [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea).

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Convertir una instalación a petición en una instalación completa

Aunque una instalación a petición permite al usuario empezar a reproducir el juego mucho antes que a una instalación completa, es posible que un usuario desee instalar explícitamente el resto del contenido del juego en el disco duro local. Es posible que el usuario desee poder jugar sin necesidad de medios de origen, o bien, puede que simplemente desee evitar los tiempos de carga más largos del juego que resultan de la instalación de contenido a petición. Si el programa de instalación del juego usa Windows Installer, el juego puede proporcionar una opción en la interfaz de usuario de opciones del juego para terminar de instalar el contenido restante. Cuando el usuario selecciona esta opción, el juego puede llamar a [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para forzar la instalación local de las características restantes. no es necesario generar una aplicación de instalación independiente para ello.

### <a name="maintenance-of-game-software-and-content"></a>Mantenimiento de software y contenido de juegos

Una de las ventajas que tienen los juegos de Windows sobre los juegos de consola es la facilidad relativa con la que el publicador puede publicar las actualizaciones del juego después de la versión inicial. Si estas actualizaciones presentan contenido nuevo o simplemente corrigen errores, es importante que el proceso de actualización sea lo más sencillo posible para el usuario final. El proceso de actualización es aún más importante para los juegos en línea, lo que normalmente requiere que todos los usuarios ejecuten la versión más reciente del juego para conectarse.

### <a name="checking-for-updates-automatically"></a>Buscar actualizaciones automáticamente

Los usuarios no deben tener que olvidar buscar revisiones. Si hay una actualización disponible para el juego, se debe notificar al usuario al menos y, idealmente, la revisión ya debe estar descargada.

Una manera sencilla de que un juego busque actualizaciones es conectarse a un servidor Web hospedado por el publicador con una dirección URL específica y descargar un archivo de texto que especifique el número de versión de la última versión disponible del juego, junto con una dirección URL desde la que descargar un paquete que actualizará el juego a la versión más reciente.

La comprobación de actualizaciones cada vez que el usuario juega el juego es adecuado para asegurarse de que el usuario está ejecutando la versión más reciente. Sin embargo, si se detecta la existencia de una nueva actualización inmediatamente antes de que el usuario intente jugar al juego, el usuario puede verse obligado a retrasar la reproducción del juego hasta que finalice la descarga de la actualización. En el caso de las actualizaciones grandes o lentas, este retraso puede estar en el orden de horas. Para evitar obligar al usuario a esperar antes de reproducir el juego, el juego puede usar Programador de tareas para programar comprobaciones periódicas de nuevas actualizaciones. Si se detecta una actualización, el juego puede empezar a descargar la actualización inmediatamente, por lo que es probable que se descargue completamente y esté lista para instalarse la próxima vez que el usuario la reproduzca.

### <a name="downloading-patches-automatically"></a>Descargar revisiones automáticamente

Una vez que el juego haya detectado que hay una nueva actualización disponible, debe empezar inmediatamente a descargar la actualización. Dado que la tarea que comprueba las actualizaciones normalmente se ejecuta silenciosamente en segundo plano, la descarga debe ser tan discreta como sea posible. El Servicio de transferencia inteligente en segundo plano (BITS) es una característica del sistema operativo que permite a las aplicaciones descargar archivos de Internet incluso mientras la aplicación no se está ejecutando. Los trabajos de descarga de BITS solo se ejecutan cuando el usuario ha iniciado sesión y solo cuando la máquina ya está conectada a la red. BITS no intenta forzar el equipo para que se conecte a la red por sí mismo. Si el usuario se desconecta de la red o cierra la sesión, el trabajo de BITS se pausa y se reanudará la descarga la próxima vez que el usuario inicie sesión y se conecte a la red. La aplicación puede configurar sus trabajos de BITS para usar solo el ancho de banda de red que, de otro modo, permanecería sin usar, con el fin de evitar que el trabajo afecte al rendimiento de otras aplicaciones que podrían estar usando la red (por ejemplo, un juego en línea). BITS está disponible en Windows XP y Windows 2000 Service Pack 3.

## <a name="other-resources"></a>Otros recursos

Para obtener más información sobre las tecnologías a las que se hace referencia en este artículo, consulte las secciones correspondientes de MSDN Library:

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Servicio de transferencia inteligente en segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (bits)

Para obtener más información sobre el uso de Windows Installer para juegos, sintonice la columna de DirectX de conducción del próximo mes, "Introducción a Windows Installer para desarrolladores de juegos".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 