---
description: Esta documentación es la principal fuente de material de referencia para Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Guía básica de Windows Installer documentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324d626eb5dd201a47c16613c5de598fcd13052d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677589"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Guía básica de Windows Installer documentación

Esta documentación es la principal fuente de material de referencia para Windows Installer. Proporciona información sobre los paquetes de instalación y el servicio de instalador. También se proporcionan descripciones completas de la interfaz de programación de aplicaciones (API) y los elementos de la base de datos del instalador. Esta documentación también contiene una explicación de ejemplos básicos de instalación y actualización de paquetes en [Windows Installer ejemplos](windows-installer-examples.md).

La [Guía basada en roles para Windows Installer documentación](role-based-guide-to-windows-installer-documentation.md) es una alternativa que se proporciona como guía a los lectores que prefieren ver vínculos a temas organizados por roles profesionales y escenarios de tareas comunes.

Para obtener información sobre Windows Installer grupos de noticias, vea también el tema: [otros orígenes de información de Windows Installer](other-sources-of-windows-installer-information.md).

Para obtener una lista de sugerencias sobre el uso del Windows Installer, consulte [prácticas recomendadas de Windows Installer](windows-installer-best-practices.md).

En la lista siguiente se describe cada sección de la documentación del instalador.

-   [Acerca de Windows Installer](about-windows-installer.md) proporciona información general sobre las funcionalidades del instalador y las ventajas, como el anuncio, la instalación a petición, la resistencia, la personalización y la administración de componentes. En esta sección se presentan los conceptos de los componentes y las características del instalador, que son esenciales para comprender cómo el instalador organiza una instalación. También se analizan varios temas de alto nivel sobre la instalación, como la Directiva del sistema, las reglas de control de versiones de archivos y la instalación de reversión.
-   El [uso de Windows Installer](using-windows-installer.md) describe diversos temas, como un método estándar para organizar una aplicación en componentes que el instalador puede instalar o quitar del equipo de un usuario. Cómo descargar un paquete de instalación desde el World Wide Web; y usando imágenes de origen comprimidas.
-   La información de las secciones novedades [en Windows Installer](what-s-new-in-windows-installer.md) se puede usar para identificar las nuevas características que no son compatibles con las versiones anteriores de Windows Installer.
-   [Firmas y Windows Installer digitales](digital-signatures-and-windows-installer.md) describe cómo se pueden usar las firmas digitales con paquetes, transformaciones, revisiones, módulos de combinación y archivos. cab externos.
-   [Ensamblados](assemblies.md) explica cómo usar Windows Installer para instalar y administrar ensamblados de Common Language Runtime y Win32.
-   La [interfaz de usuario](user-interface.md) proporciona información acerca de las capacidades de la interfaz de usuario del instalador. Aunque el instalador no proporciona una interfaz de usuario, el autor de un paquete puede mantener todos los datos y la lógica necesarios para ejecutar una interfaz de usuario interna o externa totalmente interactiva en la base de datos de instalación. En la sección de referencia se describen los elementos de la interfaz de usuario que se pueden especificar en las tablas de base de datos, incluidos los cuadros de diálogo, los controles y los eventos de control.
-   [Acciones estándar](standard-actions.md) describe las acciones estándar que usa el instalador en las tablas de secuencia para realizar una instalación. Esta información está destinada principalmente a los desarrolladores de paquetes.
-   [Acciones personalizadas](custom-actions.md) describe cómo crear funcionalidad adicional en el instalador. Las acciones personalizadas permiten a un autor de un paquete de instalación ampliar las capacidades de las acciones estándar mediante la inclusión de ejecutables, bibliotecas de vínculos dinámicos y scripts. Esta información está dirigida a los desarrolladores de paquetes que necesitan realizar funciones de instalación que no se encuentran en ningún otro lugar del instalador.
-   [Propiedades](properties.md) proporciona información sobre las propiedades que usa el instalador durante una instalación. Las secciones about y Using proporcionan información general sobre estas variables globales y cada propiedad se describe en la sección de referencia.
-   El [flujo de información de Resumen](summary-information-stream.md) documenta las propiedades de información de Resumen utilizadas por el instalador. Esta información es de interés para todos los desarrolladores.
-   [Revisiones y actualizaciones](patching-and-upgrades.md) describe el uso del instalador para realizar actualizaciones de archivos, QFE, actualizaciones secundarias, actualizaciones de productos y revisiones.
-   [Transformaciones](transforms.md) explica cómo modificar o personalizar una base de datos de instalación mediante una transformación de base de datos y cómo generar, proteger y aplicar transformaciones.
-   La [validación de paquetes](package-validation.md) describe el uso de evaluadores de coherencia internos (CIEM) para probar la coherencia interna de los paquetes de instalación que están en desarrollo.
-   Los [módulos de combinación](merge-modules.md) presentan un estándar para el diseño de los módulos de combinación. Este estándar debe ir seguido de los programadores que crean sus propios módulos de combinación, así como de los desarrolladores que tienen previsto usar el instalador para proporcionar código compartido a sus aplicaciones.
-   [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md) describe cómo usar Windows Installer para instalar y administrar componentes del instalador diseñados para ejecutarse en sistemas operativos de 64 bits.
-   [Windows Installer ejemplos](windows-installer-examples.md) incluye un ejemplo paso a paso de la creación de un paquete de instalación con una interfaz de usuario interna en [un ejemplo de instalación](an-installation-example.md). Para obtener un ejemplo de cómo crear una actualización principal para un paquete existente, vea [un ejemplo de actualización](an-upgrade-example.md). Para obtener información sobre cómo una transformación de personalización deshabilita características y agrega nuevos recursos, vea [un ejemplo de transformación de personalización](a-customization-transform-example.md). Para obtener un ejemplo de cómo crear un paquete de revisión que aplique una pequeña actualización a un paquete de instalación existente, vea [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md). Para obtener información sobre cómo localizar un paquete de instalador existente, vea [un ejemplo de localización](a-localization-example.md).
-   La [interfaz de automatización](automation-interface.md) proporciona información a los desarrolladores que desean usar la interfaz de automatización de Windows Installer.
-   [Las funciones del instalador](installer-functions.md) describen las llamadas de función a la API del instalador. Estas son las funciones a las que llaman otras aplicaciones para tener acceso a los servicios del instalador con el fin de instalar, mantener o quitar aplicaciones. Las secciones de uso incluyen discusiones sobre cómo solicitar características, iniciar instalaciones y volver a instalar los componentes que faltan mediante programación. La sección de referencia es el material de referencia principal para las funciones del servicio del instalador.
-   La [base de datos del instalador](installer-database.md) describe la base de datos de instalación. El instalador conserva toda la lógica y los datos necesarios para una instalación en una base de datos relacional que se encuentra en un archivo. msi. En la sección acerca de se proporciona información general sobre los diagramas de esquema de los principales grupos funcionales de tablas de la base de datos. En la sección Using se describe cómo trabajar con las más importantes de estas tablas. Estas secciones contienen información que es esencial para los programadores que crean paquetes de instalación o escriben herramientas de creación de paquetes. La sección de referencia contiene material de referencia completo para cada tabla de base de datos. Esta sección también contiene la referencia principal para cada una de las funciones de base de datos. El instalador usa internamente las funciones de base de datos para tener acceso a la base de datos y es especialmente interesante para los desarrolladores de herramientas de creación de paquetes del instalador.

 

 



