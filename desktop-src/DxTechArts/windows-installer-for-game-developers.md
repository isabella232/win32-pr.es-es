---
title: Windows Instalador para desarrolladores de juegos
description: En este artículo se proporciona información general sobre Windows Installer, dirigido específicamente a los desarrolladores de juegos. Para obtener documentación detallada sobre las características y api mencionadas en este artículo, consulte el SDK Windows Platform.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290395"
---
# <a name="windows-installer-for-game-developers"></a>Windows Instalador para desarrolladores de juegos

Muestra cómo Windows installer se puede usar para instalar juegos en equipos de usuario final. Windows El instalador ofrece compatibilidad completa con una interfaz de usuario personalizada, así como con la aplicación de revisiones.

Microsoft Windows Installer es la API preferida para instalar software en Windows basados en aplicaciones. Aunque muchas de las características de Windows Installer están diseñadas para admitir la implementación de aplicaciones empresariales en un entorno corporativo, Windows Installer también es completamente adecuado para instalar juegos en equipos de usuario final. Las principales ventajas de usar Windows Installer para la instalación de juegos son:

-   Desinstalación confiable
-   Capacidad de instalar contenido a petición
-   Compatibilidad con la interfaz de usuario completamente personalizada
-   Aplicación eficaz de revisiones

En este artículo se proporciona información general sobre Windows Installer, dirigido específicamente a los desarrolladores de juegos. Para obtener documentación detallada sobre las características y api mencionadas en este artículo, consulte el SDK Windows Platform.

-   [Información general](#overview)
-   [Conceptos clave Windows instalador](#key-windows-installer-concepts)
    -   [Componentes](#components)
    -   [Características](#features)
-   [Estados de instalación](#install-states)
-   [Instalación a petición](#install-on-demand)
-   [Personalización de la interfaz de usuario](#custom-user-interface)
-   [Aplicación de revisiones](#patching)
-   [Otros recursos](#other-resources)

## <a name="overview"></a>Información general

Todas las Windows basadas en el instalador usan un archivo de base de datos de instalación denominado archivo MSI para describir cómo se va a instalar la aplicación. El archivo MSI contiene información sobre qué archivos, claves del Registro, accesos directos de escritorio, asociaciones de archivos y otros elementos de la aplicación se van a instalar. Los archivos reales que se instalarán se pueden comprimir en el propio archivo MSI, empaquetarse y comprimirse en "archivos contenedor" independientes, o almacenarse en otro lugar en el medio de instalación como archivos individuales sin comprimir. El archivo MSI también puede hacer referencia a acciones personalizadas implementadas externamente, con el fin de permitir acciones para las que el archivo MSI no permite de forma nativa.

Opcionalmente, un archivo MSI puede contener una interfaz de usuario para guiar al usuario a través del proceso de instalación. Esta interfaz de usuario es adecuada para la mayoría de las aplicaciones. Sin embargo, tiene la apariencia de una aplicación de Windows normal y muchos desarrolladores de juegos prefieren que su aplicación de configuración mantenga la apariencia del juego en sí, con el fin de proporcionar una experiencia de usuario final más coherente. Para admitir este escenario de interfaz de usuario totalmente personalizada, una aplicación de instalación puede desactivar la interfaz de usuario integrada de Windows Installer y controlar toda la interfaz de usuario. La API Windows Installer expone un mecanismo de devolución de llamada para permitir que se notifique a una interfaz de usuario de instalación personalizada del progreso de la instalación, así como eventos importantes como solicitudes de cambio de disco.

Windows El instalador no es una solución de un extremo a otro para crear configuraciones. Solo es una API que un programa de instalación puede usar para realizar la instalación real de archivos, claves del Registro, accesos directos de escritorio y otros elementos de la aplicación. Las versiones recientes de todas las principales herramientas de instalación comercial (por ejemplo, InstallShield, WISE y Microsoft Visual Studio) admiten Windows Instalador. Estas herramientas proporcionan interfaces de usuario prácticas para crear la configuración de un juego, pero se basan en Windows Installer API para realizar gran parte de la instalación real. Estas herramientas también se pueden usar solo para compilar una base de datos MSI que contenga el paquete de instalación, que luego se puede instalar desde una interfaz de usuario de instalación personalizada escrita. Como alternativa a las herramientas de terceros, la API del instalador de Windows proporciona todas las funciones necesarias para crear y manipular una base de datos MSI mediante programación, y el SDK de plataforma de Windows incluye una herramienta de edición de bases de datos MSI sin sistema completo denominada Orca.

## <a name="key-windows-installer-concepts"></a>Conceptos clave Windows instalador

Estos son los componentes y características Windows Installer.

### <a name="components"></a>Componentes

Una aplicación se forma de uno o varios componentes, identificados por un identificador de componente GUID. Un componente es una unidad atómica; está completamente instalado o no está instalado en absoluto. Un componente puede constar de un único archivo, varios archivos, claves del Registro, accesos directos de escritorio o alguna combinación de ellos. Los recursos (archivos, entre otros) dentro de un componente deben ser únicos para ese componente; no hay dos componentes que puedan contener el mismo recurso. Un componente nunca se instala explícitamente; solo se instala como parte de una característica (consulte a continuación).

### <a name="features"></a>Características

Una característica es un grupo de componentes, identificados por un identificador de característica GUID. A diferencia de los componentes, varias características pueden contener el mismo componente. Un componente compartido entre varias características se instalará si alguna de esas características está instalada y se quitará solo cuando se hayan desinstalado todas las características que hacen referencia al componente. La instalación de una característica se puede realizar automáticamente como parte de la instalación de un producto, o bien se puede realizar manualmente mediante la API [**MsiConfigureFeature.**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)

Aunque algunos juegos tienen varias "características" que se pueden instalar de forma independiente, el concepto Windows Installer de una característica sigue siendo útil. Puesto que una característica del instalador de Windows no es más que una colección de componentes que se pueden instalar juntos, los juegos pueden usar características para agrupar todo el contenido necesario para una fase determinada del juego. Por ejemplo, un juego orientado a niveles podría definir una característica por nivel, que consta de todo el contenido necesario para ese nivel. Esto permitiría al juego instalar el contenido de un nivel a la vez desde dentro del propio juego, en lugar de instalar todo el contenido para todos los niveles durante la instalación inicial.

## <a name="install-states"></a>Estados de instalación

Cada componente o característica tiene un estado de instalación asociado, que determina si el componente o característica está disponible y, si es así, dónde están instalados los archivos del componente o característica. Los posibles estados de instalación de una característica son:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Ausente
</dt> <dd>

La característica no está instalada y, por tanto, es inaccesible.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Local
</dt> <dd>

La característica está disponible y se instala para ejecutarse desde el disco duro local.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuente
</dt> <dd>

La característica está disponible y se instala para ejecutarse desde el medio de origen original (normalmente un CD o DVD).

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Anunciado
</dt> <dd>

La característica no está instalada, pero se puede instalar a petición mediante la API [**MsiConfigureFeature.**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) Cuando la característica está realmente instalada, se puede instalar en el estado Local o Source.

</dd> </dl>

Un componente puede tener cualquiera de los estados anteriores, excepto "Anunciado". Si un componente forma parte de una característica anunciada, el componente aparecerá como "Absent" hasta que se instale la característica.

## <a name="install-on-demand"></a>Instalación a petición

Windows El instalador permite que una aplicación marque las características como Anunciadas, lo que significa que la característica aún no está instalada, pero está disponible para instalarse en tiempo de ejecución si es necesario. La instalación de características en tiempo de ejecución se conoce como "Instalación a petición". Los juegos pueden usar Instalar a petición para reducir drásticamente el tiempo necesario para la configuración inicial del juego aplazando la instalación del contenido del juego hasta que sea necesario en tiempo de ejecución. El retraso necesario para instalar el contenido en tiempo de ejecución a menudo se puede ocultar parcial o completamente realizando la instalación a petición en un subproceso en segundo plano, mientras que el usuario está ocupado con el juego.

## <a name="custom-user-interface"></a>Personalización de la interfaz de usuario

Aunque Windows Installer proporciona una interfaz de usuario predeterminada que guía al usuario a través de la instalación de la aplicación, esta interfaz es similar a la de una aplicación Windows estándar. Muchos desarrolladores de juegos prefieren que su interfaz de usuario de instalación tenga el mismo aspecto que el juego en sí, para proporcionar al usuario una sensación de la comodidad del juego. Para admitir esto, Windows Installer permite deshabilitar completamente su interfaz de usuario integrada, lo que permite al desarrollador proporcionar una interfaz de usuario completamente personalizada.

El programa de instalación personalizada deshabilita primero Windows interfaz de usuario integrada del instalador mediante la API [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) para establecer el nivel de interfaz de usuario en INSTALLUILEVEL \_ NONE. A continuación, llama a la API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) para especificar una función de devolución de llamada a la que se llamará durante el proceso de instalación para notificar al programa de instalación los eventos clave durante la instalación.

A continuación, se inicia el proceso de instalación real mediante una llamada a la API [**MsiInstallProduct.**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) Esta API acepta una cadena de parámetro que permite al autor de la llamada especificar valores para las propiedades con nombre. Estas propiedades se pueden usar dentro de la propia base de datos de instalación para personalizar cómo se va a instalar la aplicación. Estas propiedades se pueden usar para especificar:

-   Directorio en el que se va a instalar la aplicación
-   Qué características se van a instalar localmente y cuáles se van a instalar para ejecutarse desde el CD/DVD (por ejemplo, para habilitar la elección entre una instalación mínima y una instalación completa).
-   Si la aplicación debe instalarse para todos los usuarios de la máquina o solo para el usuario actual

Durante el transcurso de la instalación, el programa de instalación usa los mensajes de notificación enviados a su función de devolución de llamada para determinar cuándo actualizar la interfaz de usuario del indicador de progreso, cuándo solicitar al usuario que inserte el siguiente CD o cuándo notificar al usuario un error en el proceso de instalación.

## <a name="patching"></a>Aplicación de revisiones

Windows El instalador permite aplicar revisiones a las aplicaciones instaladas mediante la aplicación de un archivo de revisión. Un archivo de revisión contiene los nuevos archivos que va a agregar la revisión, los archivos modificados por la revisión y una lista de los cambios que se deben realizar en la base de datos de instalación. Para ahorrar espacio, en lugar de almacenar el contenido completo de un archivo modificado por la revisión, el archivo de revisión contiene realmente solo las diferencias entre la versión original del archivo y la nueva versión del archivo.

Para crear una revisión, necesita la imagen de instalación para cada una de las versiones de la aplicación desde las que desea actualizar la revisión, así como la imagen de instalación de la nueva versión actualizada de la aplicación. Una imagen de instalación consta de la base de datos MSI y todos los archivos de datos reales de la aplicación. La mejor manera de crear una imagen de instalación para una nueva versión de la aplicación es copiar la imagen de instalación de la versión anterior de la aplicación y, a continuación, realizar los cambios necesarios para actualizar esa copia a la versión con revisión.

Una vez que tenga todas las imágenes de configuración necesarias, puede crear las revisiones mediante Msimsp.exe, que es una herramienta de creación de revisiones disponible como parte del SDK de plataforma. La herramienta pedirá las ubicaciones de cada una de las imágenes de instalación y, a continuación, determinará cómo representar eficazmente las diferencias entre las versiones sucesivas. La salida de la herramienta es el archivo de revisión final (identificado por el MSP de extensión). Para instalar la revisión mediante programación, llame a la API [**MsiApplyPatch.**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) El usuario también puede instalar la revisión manualmente haciendo doble clic en el archivo MSP en el Explorador.

## <a name="other-resources"></a>Otros recursos

-   Para obtener información detallada sobre la API Windows Installer, [consulte Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Para obtener información sobre los procedimientos recomendados para la instalación de juegos, consulte [Instalación y mantenimiento de juegos.](/windows/desktop/DxTechArts/installation-and-maintenance-of-games)

 

 