---
title: Windows Installer para desarrolladores de juegos
description: En este artículo se proporciona información general de Windows Installer, específicamente destinada a desarrolladores de juegos. Para obtener documentación detallada sobre las características y las API mencionadas en este artículo, consulte el SDK de la plataforma Windows.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44227b633f7f9491b8a69bc06aa7945941a154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420966"
---
# <a name="windows-installer-for-game-developers"></a>Windows Installer para desarrolladores de juegos

Muestra cómo se puede usar Windows Installer para instalar juegos en equipos de usuario final. Windows Installer ofrece compatibilidad total para una interfaz de usuario personalizada, así como para aplicar revisiones.

Microsoft Windows Installer es la API preferida para instalar software en equipos basados en Windows. Aunque muchas de las características de Windows Installer están diseñadas para admitir la implementación de aplicaciones empresariales en un entorno corporativo, Windows Installer también es totalmente adecuado para instalar juegos en equipos de usuario final. Las principales ventajas de usar Windows Installer para la instalación de juegos son:

-   Desinstalación confiable
-   Capacidad para instalar contenido a petición
-   Compatibilidad con la interfaz de usuario completamente personalizada
-   Revisión eficaz

En este artículo se proporciona información general de Windows Installer, específicamente destinada a desarrolladores de juegos. Para obtener documentación detallada sobre las características y las API mencionadas en este artículo, consulte el SDK de la plataforma Windows.

-   [Información general](#overview)
-   [Conceptos de Windows Installer clave](#key-windows-installer-concepts)
    -   [Componentes](#components)
    -   [Características](#features)
-   [Estados de instalación](#install-states)
-   [Instalación a petición](#install-on-demand)
-   [Personalización de la interfaz de usuario](#custom-user-interface)
-   [Revisiones](#patching)
-   [Otros recursos](#other-resources)

## <a name="overview"></a>Información general

Todas las configuraciones basadas en Windows Installer usan un archivo de base de datos de instalación denominado archivo MSI para describir cómo se va a instalar la aplicación. El archivo MSI contiene información sobre qué archivos, claves del registro, accesos directos del escritorio, asociaciones de archivos y otros elementos de la aplicación se van a instalar. Los archivos reales que se van a instalar pueden comprimirse en el propio archivo MSI, empaquetarse y comprimirse en "archivos. cab" independientes, o almacenarse en otro lugar del medio de instalación como archivos individuales sin comprimir. El archivo MSI también puede hacer referencia a acciones personalizadas implementadas externamente, con el fin de permitir acciones para las que el archivo MSI no permite de forma nativa.

Un archivo MSI puede contener opcionalmente una interfaz de usuario para guiar al usuario a través del proceso de instalación. Esta interfaz de usuario es adecuada para la mayoría de las aplicaciones. Sin embargo, tiene la apariencia de una aplicación Windows normal y muchos desarrolladores de juegos prefieren que su aplicación de configuración mantenga la apariencia del propio juego, con el fin de proporcionar una experiencia de usuario final más coherente. Para admitir este escenario de interfaz de usuario totalmente personalizada, una aplicación de instalación puede desactivar la interfaz de usuario integrada de Windows Installer y administrar toda la interfaz de usuario. La API de Windows Installer expone un mecanismo de devolución de llamada para permitir que una interfaz de usuario de instalación personalizada reciba notificaciones sobre el progreso de la instalación, así como eventos importantes, como las solicitudes de cambio de disco.

Windows Installer no es una solución de un extremo a otro para la creación de configuraciones. Solo es una API que puede utilizar un programa de instalación para realizar la instalación real de archivos, claves del registro, accesos directos del escritorio y otros elementos de la aplicación. Las versiones recientes de todas las principales herramientas de configuración comercial (por ejemplo, InstallShield, WISE y Microsoft Visual Studio) admiten Windows Installer. Estas herramientas proporcionan interfaces de usuario prácticas para crear el programa de instalación de un juego, pero dependen de la API de Windows Installer para realizar gran parte de la instalación real. Estas herramientas también se pueden usar para crear una base de datos MSI que contenga el paquete de instalación, que se puede instalar después desde una interfaz de usuario de instalación personalizada. Como alternativa a las herramientas de terceros, la API de Windows Installer proporciona todas las funciones necesarias para crear y manipular una base de datos de MSI mediante programación, y el SDK de la plataforma Windows incluye una herramienta de edición de base de datos MSI básica denominada orca.

## <a name="key-windows-installer-concepts"></a>Conceptos de Windows Installer clave

Estos son los componentes y características de Windows Installer.

### <a name="components"></a>Componentes

Una aplicación se compone de uno o más componentes, identificados mediante un identificador de componente GUID. Un componente es una unidad atómica; está completamente instalado o no está instalado. Un componente puede constar de un solo archivo, varios archivos, claves del registro, métodos abreviados de escritorio o alguna combinación de ellos. Los recursos (archivos, etc.) de un componente deben ser únicos para ese componente; dos componentes no pueden contener el mismo recurso. Un componente nunca se instala explícitamente. solo se instala como parte de una característica (consulte a continuación).

### <a name="features"></a>Características

Una característica es un grupo de componentes, identificado por un identificador de característica de GUID. A diferencia de los componentes de, varias características pueden contener el mismo componente. Se instalará un componente compartido entre varias características si alguna de esas características está instalada y se quitará solo cuando se hayan desinstalado todas las características que hacen referencia al componente. La instalación de una característica puede realizarse automáticamente como parte de la instalación de un producto, o bien puede realizarse manualmente mediante la API de [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) .

Aunque pocos juegos tienen varias "características" que se pueden instalar de forma independiente, el concepto de Windows Installer de una característica sigue siendo útil. Puesto que una característica Windows Installer no es más que una colección de componentes que se pueden instalar juntos, los juegos pueden usar características para agrupar todo el contenido necesario para una fase determinada del juego. Por ejemplo, un juego orientado a niveles podría definir una característica por nivel, que consiste en todo el contenido necesario para ese nivel. Esto permitiría al juego instalar el contenido de un nivel a la vez desde dentro del propio juego, en lugar de instalar todo el contenido de todos los niveles durante la instalación inicial.

## <a name="install-states"></a>Estados de instalación

Cada componente o característica tiene un estado de instalación asociado, que determina si el componente o característica está disponible, y si es así, donde se instalan los archivos del componente o característica. Los posibles estados de instalación de una característica son:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Existe
</dt> <dd>

La característica no está instalada y, por tanto, no se puede obtener acceso a ella.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Localizar
</dt> <dd>

La característica está disponible y se instala para ejecutarse desde el disco duro local.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes
</dt> <dd>

La característica está disponible y se instala para ejecutarse desde el medio de origen original (normalmente un CD o DVD).

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Anunciados
</dt> <dd>

La característica no está instalada, pero se puede instalar a petición mediante la API de [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) . Una vez instalada la característica, se puede instalar en el estado local o de origen.

</dd> </dl>

Un componente puede tener cualquiera de los Estados anteriores excepto "anunciado". Si un componente forma parte de una característica anunciada, el componente aparecerá como "ausente" hasta que se instale la característica.

## <a name="install-on-demand"></a>Instalación a petición

Windows Installer permite que una aplicación Marque características como anunciadas, lo que significa que la característica aún no está instalada, pero está disponible para instalar en tiempo de ejecución si es necesario. La instalación de características en tiempo de ejecución se conoce como "instalar a petición". Los juegos pueden utilizar la instalación a petición para reducir drásticamente el tiempo necesario para la configuración inicial del juego al aplazar la instalación del contenido del juego hasta que sea necesario en tiempo de ejecución. El retraso necesario para instalar el contenido en tiempo de ejecución se puede ocultar a menudo parcial o totalmente mediante la instalación a petición en un subproceso en segundo plano, mientras que el usuario está ocupado con el juego.

## <a name="custom-user-interface"></a>Personalización de la interfaz de usuario

Aunque Windows Installer proporciona una interfaz de usuario predeterminada que guía al usuario a través de la instalación de la aplicación, esta interfaz es similar a la de una aplicación Windows estándar. Muchos desarrolladores de juegos prefieren que su interfaz de usuario de instalación tenga el mismo aspecto y funcionamiento que el propio juego, para proporcionar al usuario una idea de los Ambiance del juego. Para admitir esto, Windows Installer permite que su interfaz de usuario integrada esté completamente deshabilitada, lo que permite al desarrollador proporcionar una interfaz de usuario completamente personalizada.

En primer lugar, el programa de instalación personalizado deshabilita la interfaz de usuario integrada de Windows Installer mediante la API de [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) para establecer el nivel de la interfaz de usuario en INSTALLUILEVEL \_ None. A continuación, llama a la API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) para especificar una función de devolución de llamada a la que se llamará durante el proceso de instalación con el fin de notificar al programa de instalación los eventos clave durante la instalación.

El proceso de instalación real se inicia mediante una llamada a la API [**MsiInstallProduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) . Esta API acepta una cadena de parámetro que permite al llamador especificar valores para las propiedades con nombre. Estas propiedades se pueden usar en la base de datos de instalación para personalizar cómo se va a instalar la aplicación. Estas propiedades se pueden utilizar para especificar:

-   Directorio en el que se va a instalar la aplicación.
-   Las características que se van a instalar localmente y que se instalarán para ejecutarse desde el CD/DVD (por ejemplo, para habilitar la selección entre una instalación mínima y una instalación completa)
-   Si la aplicación debe instalarse para todos los usuarios del equipo o solo para el usuario actual

Durante el transcurso de la instalación, el programa de instalación utiliza los mensajes de notificación enviados a su función de devolución de llamada para determinar cuándo actualizar su interfaz de usuario del indicador de progreso, Cuándo se le pedirá al usuario que inserte el siguiente CD, o Cuándo notificará al usuario un error en el proceso de instalación.

## <a name="patching"></a>Aplicación de revisiones

Windows Installer permite revisar las aplicaciones instaladas aplicando un archivo de revisión. Un archivo de revisión contiene los nuevos archivos que va a agregar la revisión, los archivos modificados por la revisión y una lista de cambios que se deben realizar en la base de datos de instalación. Para ahorrar espacio, en lugar de almacenar el contenido completo de un archivo modificado por la revisión, el archivo de revisión contiene realmente solo las diferencias entre la versión original del archivo y la nueva versión del archivo.

Para crear una revisión, necesita la imagen de instalación para cada una de las versiones de la aplicación de la que desea que se actualice la revisión, así como la imagen de configuración de la nueva versión actualizada de la aplicación. Una imagen de instalación consta de la base de datos MSI y de todos los archivos de datos reales de la aplicación. La mejor manera de crear una imagen de instalación para una nueva versión de la aplicación es copiar la imagen de instalación de la versión anterior de la aplicación y, a continuación, realizar los cambios necesarios para actualizar esa copia a la versión revisada.

Una vez que tenga todas las imágenes de instalación necesarias, puede crear las revisiones mediante Msimsp.exe, que es una herramienta de creación de revisiones disponible como parte del SDK de la plataforma. La herramienta le pedirá las ubicaciones de cada una de las imágenes de instalación y, a continuación, determinará cómo representar eficazmente las diferencias entre las versiones sucesivas. La salida de la herramienta es el archivo de revisión final (identificado por la extensión MSP). Para instalar el parche mediante programación, llame a la API [**MsiApplyPatch**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) . El usuario también puede instalar la revisión manualmente si hace doble clic en el archivo MSP en el explorador.

## <a name="other-resources"></a>Otros recursos

-   Para obtener información detallada sobre la API de Windows Installer, vea [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Para obtener información sobre los procedimientos recomendados para la instalación de juegos, consulte [instalación y mantenimiento de juegos](/windows/desktop/DxTechArts/installation-and-maintenance-of-games).

 

 