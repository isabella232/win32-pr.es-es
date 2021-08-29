---
title: Instalación y mantenimiento de juegos
description: En este artículo se describe un conjunto de procedimientos recomendados que pueden ayudar a reducir la frustración de los usuarios sobre el tiempo necesario para instalar un juego, evitar llamadas de soporte técnico innecesarias y permitir que los usuarios empiecen a jugar a su juego lo más rápido y sin problemas posible.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57518a0eb2c0d9dc07497e8c530394469df0354c321414191e6d07385352992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830505"
---
# <a name="installation-and-maintenance-of-games"></a>Instalación y mantenimiento de juegos

En este artículo se describe un conjunto de procedimientos recomendados que pueden ayudar a reducir la frustración de los usuarios sobre el tiempo necesario para instalar un juego, evitar llamadas de soporte técnico innecesarias y permitir que los usuarios empiecen a jugar a su juego lo más rápido y sin problemas posible.

-   [Instalación inicial](#initial-installation)
    -   [Streamlining the Installation UI](#streamlining-the-installation-ui)
    -   [Reducir el tiempo necesario para la instalación](#reducing-the-time-required-for-installation)
    -   [Instalación mínima](#minimal-installation)
    -   [Instalación a petición](#install-on-demand)
-   [Juego posterior a la instalación](#post-installation-game-play)
    -   [Autorun](#autorun)
    -   [Convertir una instalación a petición en una instalación completa](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Mantenimiento del software y el contenido del juego](#maintenance-of-game-software-and-content)
    -   [Buscar actualizaciones automáticamente](#checking-for-updates-automatically)
    -   [Descargar revisiones automáticamente](#downloading-patches-automatically)
-   [Otros recursos](#other-resources)
-   [Temas relacionados](#related-topics)

## <a name="initial-installation"></a>Instalación inicial

Los usuarios compran juegos porque les gusta jugar a ellos, no porque disfruten de instalarlos. La instalación de un juego debe ser lo más rápida, sencilla y sencilla posible para el usuario final. Lo ideal es que los usuarios finales ni siquiera vean una interfaz de usuario de instalación. deben poder simplemente colocar el disco del juego en la bandeja y empezar a jugar.

### <a name="streamlining-the-installation-ui"></a>Streamlining the Installation UI

Los aspectos comunes de las URI de instalación de juegos existentes interfieren con la experiencia del usuario final deseada:

-   Hacer preguntas innecesarias al usuario.

    Por ejemplo, muchos juegos preguntan si el usuario quiere instalar DirectX. Si el juego requiere la ejecución de Microsoft DirectX y la versión correcta de DirectX aún no está instalada, el juego simplemente debe instalar DirectX.

-   Hacer preguntas al usuario que una gran mayoría de los usuarios responderá de la misma manera.

    Para los usuarios típicos, la configuración predeterminada para la ruta de instalación, menú Inicio ubicación, y así sucesivamente, son correctas. Ofrezca opciones avanzadas para los usuarios que desean cambiar esta configuración.

La interfaz de usuario de instalación debe estar diseñada para permitir que el usuario típico empiece a jugar al juego lo antes posible. Si AutoRun está habilitado en el equipo del usuario, que es el valor predeterminado, el programa de instalación debe asumir que el usuario quiere jugar al juego lo antes posible, omitiendo las preguntas innecesarias. El programa de instalación[Instalar](#install-on-demand)a petición m debe empezar a instalar el juego en la ruta de instalación predeterminada, preferiblemente mediante una configuración como la descrita en . Es adecuado ofrecer a los usuarios la oportunidad de cambiar la configuración de instalación antes de iniciar automáticamente la instalación. Sin embargo, esto debe realizarse solicitando al usuario que presione una tecla para las opciones de configuración avanzadas y, a continuación, continuar automáticamente con las opciones predeterminadas si el usuario no pulsa esa clave en un plazo de entre cinco y diez segundos.

Si AutoRun no está habilitado en el equipo del usuario, el programa de instalación debe suponer que el usuario no quiere que el programa de instalación comience a instalar el juego automáticamente. Si el programa de instalación se inicia por algún medio distinto de AutoRun, debe iniciar la interfaz de usuario de configuración avanzada.

### <a name="reducing-the-time-required-for-installation"></a>Reducir el tiempo necesario para la instalación

La mayoría de los Windows de Microsoft en la actualidad pueden tardar entre cinco minutos y media hora en finalizar el proceso de instalación. Por el contrario, la mayoría de los juegos de consola no toman más de treinta segundos desde el momento en que el usuario inserta el CD del juego hasta el momento en que el usuario puede jugar al juego. Esta diferencia se debe al hecho de que la mayoría de los Windows están diseñados para ejecutar la mayor parte de su contenido desde la unidad de disco duro del equipo, si no todo. Las consolas, que carecen de un lugar para almacenar permanentemente grandes cantidades de contenido, requieren que el contenido se ejecute desde los medios de origen. Aunque la carga de contenido desde la unidad de disco duro local permite tiempos de carga más rápidos en el juego, la desventaja es que todo ese contenido debe copiarse desde el medio de origen a la unidad de disco duro en algún momento. La Windows los juegos deciden copiar todo el contenido en la unidad de disco duro a la vez, como parte de un proceso de instalación. Esto disminuye la experiencia inicial del usuario con el juego al hacer que el usuario vea una barra de progreso durante varios minutos antes de poder jugar.

Hay dos enfoques que se pueden usar para minimizar el tiempo invertido inicialmente en la instalación del [juego:](#minimal-installation) instalación mínima e [instalación a petición.](#install-on-demand)

### <a name="minimal-installation"></a>Instalación mínima

En un escenario de instalación mínima, el juego instala solo un conjunto mínimo de contenido en el disco duro. Normalmente, se compone solo del archivo ejecutable y los archivos DLL del juego. El resto del contenido se accede directamente desde los medios de origen. Esto reduce drásticamente el tiempo necesario para la instalación, ya que el archivo ejecutable de un juego rara vez es mayor que 10-20 MB. El inconveniente es que el juego tarda más tiempo en cargar contenido durante el juego, ya que debe cargarlo desde los medios de origen más lentos.

Para crear una configuración de instalación mínima en una Windows basada en el instalador:

-   Agrupa todos los componentes que se instalarán en la unidad de disco duro en una característica marcada para instalarse localmente.

    Esta característica se denominará característica "Bootstrap".

-   Agrupa todos los componentes que se van a ejecutar desde el medio de origen en una característica marcada como "ejecutar desde el origen".
-   Al abrir un archivo que podría estar en el medio de origen, use la función [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar la ruta de acceso al archivo, en lugar de codificar de forma rígida la ruta de acceso.

    Al hacerlo, se garantiza que el archivo se puede encontrar incluso si cambia la letra de unidad de la unidad de CD/DVD del usuario.

-   Comprima el contenido que permanece en el CD/DVD.

    La cantidad de tiempo de CPU invertido en descomprimir el contenido normalmente se ocultará por la velocidad de transferencia lenta de datos de la unidad de CD/DVD.

-   Agrupa el contenido en archivos grandes y contiguos y accede a él en orden secuencial.

    Los tiempos de búsqueda de las unidades de CD/DVD son abismales en comparación con los de las unidades de disco duro y la mayoría de las unidades de CD/DVD no alcanzan las tasas máximas de transferencia a menos que estén leyendo un archivo grande y contiguo.

-   Descándalo en el CD/DVD en el orden en que es probable que se pueda acceder a él.

    Los tiempos de búsqueda se reducen considerablemente cuando se accede a los archivos en el mismo orden que su diseño en disco.

### <a name="install-on-demand"></a>Instalación a petición

En un escenario de instalación a petición, como para una instalación mínima, el juego se instala inicialmente en el disco duro solo los archivos necesarios para iniciar el juego. Sin embargo, en lugar de acceder al contenido restante desde los medios de origen cada vez que se necesita, el juego instala realmente cada fragmento de contenido en la unidad de disco duro según sea necesario por primera vez y, a continuación, accede a él desde la unidad de disco duro local en cada uso posterior. El tiempo necesario para la instalación inicial es tan pequeño como en para una instalación mínima, pero después de la primera vez que se accede a cada fragmento de contenido, los tiempos de carga mejoran.

Para crear una configuración de instalación a petición en una Windows basada en el instalador:

-   Agrupa todos los componentes que se instalarán inicialmente en la unidad de disco duro en una característica marcada para instalarse localmente.

    Tenga en cuenta que esto es idéntico a la característica Bootstrap para una instalación mínima.

-   Agrupa el contenido restante en varias características en función de los componentes que es probable que se utilicen juntos.

    Por ejemplo, en un juego basado en niveles, a agrupar todo el contenido usado en un nivel determinado en una sola característica. Tenga en cuenta que Windows Installer permite que varias características compartan un componente, por lo que si tiene contenido que se usa en varios niveles, puede agregar ese contenido a las características de todos los niveles necesarios sin replicar el contenido. Todas estas características deben marcarse como "Anunciadas", lo que significa que no se instalarán inicialmente, pero se pueden instalar más adelante según sea necesario.

-   Cuando se necesite un archivo, compruebe primero si el archivo ya está instalado mediante la función [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea).

    Si aún no está instalado (es decir, su estado es INSTALLSTATE ADVERTISED), llame a la función \_ [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar la característica localmente. Al abrir el archivo después de instalarlo, llame a [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar la ruta de acceso al archivo. Aunque no es estrictamente necesario para este escenario (ya que el contenido siempre se instalará en la unidad de disco duro antes de su uso), esto facilita la compatibilidad con una instalación mínima además de la instalación a petición.

-   Si es posible, anticipe qué contenido es probable que se necesite pronto e instállo en segundo plano durante el tiempo de inactividad.

    La instalación en segundo plano es más adecuada cuando el juego está en un punto que no necesita cada última onza de rendimiento fuera del equipo; por ejemplo, mientras se muestra una película de introducción, una escena de corte, un menú, y así sucesivamente.

-   Cree una opción en el menú de opciones del juego para forzar la instalación de todo el contenido restante.

    Para implementar esto, cree una característica que sea primaria de todas las características de instalación a petición y, a continuación, llame a [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar esta característica maestra localmente. Esto hará que las subatures también se instalen localmente.

-   El diseño del contenido debe ser similar al de una instalación mínima, salvo que el contenido debe estar agrupado solo con otro contenido que es probable que sea necesario al mismo tiempo (por ejemplo, todo el contenido de un nivel debe estar junto).

## <a name="post-installation-game-play"></a>Posteriores a la instalación Game-Play

### <a name="autorun"></a>Autorun

Para jugar a un juego que ya está instalado, el usuario solo debe quitar el disco de instalación en la bandeja de unidades. Lo primero que debe hacer el ejecutable AutoRun en el disco es comprobar si el juego ya está instalado y, si es así, iniciar el juego. Suponiendo que el juego se instaló mediante una configuración basada en Windows Installer, la comprobación para determinar si el juego está instalado se puede realizar con una sola llamada a la función [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea).

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Convertir una instalación a petición en una instalación completa

Aunque una instalación a petición permite al usuario empezar a jugar al juego mucho antes que una instalación completa, es posible que un usuario quiera instalar explícitamente el resto del contenido del juego en el disco duro local. Es posible que el usuario quiera poder jugar al juego sin necesidad de los medios de origen, o puede que simplemente quiera evitar los tiempos de carga más largos en el juego que resultan de la instalación de contenido a petición. Si la configuración del juego usa Windows Installer, el juego puede proporcionar una opción en la interfaz de usuario de opciones del juego para terminar de instalar el contenido restante. Cuando el usuario selecciona esta opción, el juego puede llamar a [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para forzar la instalación local de las características restantes. no es necesario generar una aplicación de configuración independiente para ello.

### <a name="maintenance-of-game-software-and-content"></a>Mantenimiento del software y el contenido del juego

Una de las ventajas que Windows los juegos de consola es la facilidad relativa con la que el editor puede publicar actualizaciones del juego después de su lanzamiento inicial. Tanto si estas actualizaciones introducen contenido nuevo como si simplemente corrigen errores, es importante que el proceso de actualización sea lo más fácil posible para el usuario final. El proceso de actualización es aún más importante para los juegos en línea, que normalmente requieren que todos los usuarios ejecuten la versión más reciente del juego para conectarse.

### <a name="checking-for-updates-automatically"></a>Buscar actualizaciones automáticamente

Los usuarios no deben tener que recordar ir a buscar revisiones. Si hay una actualización disponible para el juego, al menos se debe notificar al usuario y, idealmente, la revisión ya debe descargarse.

Una manera sencilla de que un juego busque actualizaciones es conectarse a un servidor web hospedado por el publicador mediante una dirección URL específica y descargar un archivo de texto que especifique el número de versión de la versión más reciente disponible del juego, junto con una dirección URL desde la que descargar un paquete que actualizará el juego a la versión más reciente.

La comprobación de las actualizaciones cada vez que el usuario realiza el juego es adecuada para asegurarse de que el usuario ejecuta la versión más reciente. Sin embargo, si la existencia de una nueva actualización se detecta inmediatamente antes de que el usuario intente jugar al juego, es posible que el usuario se ve obligado a retrasar la reproducción del juego hasta que la actualización haya terminado de descargarse. En el caso de las actualizaciones grandes o las conexiones lentas, este retraso puede estar en el orden de las horas. Para evitar forzar al usuario a esperar antes de jugar, el juego puede usar Programador de tareas para programar comprobaciones periódicas de nuevas actualizaciones. Si se detecta una actualización, el juego puede empezar a descargar la actualización inmediatamente, de modo que es probable que esté completamente descargada y lista para instalarse la próxima vez que el usuario haga el juego.

### <a name="downloading-patches-automatically"></a>Descargar revisiones automáticamente

Una vez que el juego ha detectado que hay disponible una nueva actualización, debería empezar inmediatamente a descargar la actualización. Dado que la tarea que comprueba si hay actualizaciones se ejecuta normalmente de forma silenciosa en segundo plano, la descarga debe ser lo más discreta posible. El Servicio de transferencia inteligente en segundo plano (BITS) es una característica del sistema operativo que permite a las aplicaciones descargar archivos de Internet aunque la propia aplicación no se esté ejecutando. Los trabajos de descarga de BITS solo se ejecutan cuando el usuario ha iniciado sesión y solo cuando la máquina ya está conectada a la red. BITS no intentará forzar a la máquina a conectarse a la red por sí misma. Si el usuario se desconecta de la red o se cierra, el trabajo de BITS se pausa y reanudará la descarga la próxima vez que el usuario inicie sesión y se conecte a la red. La aplicación puede configurar sus trabajos de BITS para usar solo el ancho de banda de red que, de lo contrario, permanecería sin usar, con el fin de evitar que el trabajo afectara al rendimiento de cualquier otra aplicación que pudiera estar usando la red (por ejemplo, un juego en línea). BITS está disponible en Windows XP y Windows 2000 Service Pack 3.

## <a name="other-resources"></a>Otros recursos

Para obtener más información sobre las tecnologías a las que se hace referencia en este artículo, consulte las secciones pertinentes de MSDN Library:

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Servicio de transferencia inteligente en segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (BITS)

Para obtener más información sobre el uso de Windows Installer para juegos, ajuste a la columna Driving DirectX del mes siguiente, "Introduction to Windows Installer for Game Developers" (Introducción a Windows Installer para desarrolladores de juegos).

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

 

 