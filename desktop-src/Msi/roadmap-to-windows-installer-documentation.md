---
description: Esta documentación es el origen principal del material de referencia para Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Guía básica para Windows instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625915"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Guía básica para Windows instalador

Esta documentación es el origen principal del material de referencia para Windows Installer. Proporciona información sobre los paquetes de instalación y el servicio de instalador. También proporciona descripciones completas de la interfaz de programación de aplicaciones (API) y los elementos de la base de datos del instalador. Esta documentación también contiene una explicación de ejemplos básicos de paquetes de instalación y actualización en Windows [Ejemplos del instalador .](windows-installer-examples.md)

La Guía basada en roles [para Windows Installer](role-based-guide-to-windows-installer-documentation.md) es una alternativa que se proporciona como guía para los lectores que prefieren ver vínculos a temas organizados por roles profesionales y escenarios de tareas comunes.

Para obtener información sobre Windows de noticias del Instalador de aplicaciones, vea también el tema: Otros orígenes [de Windows información del instalador .](other-sources-of-windows-installer-information.md)

Para obtener una lista de sugerencias sobre cómo usar Windows Installer, vea [Windows Installer Best Practices](windows-installer-best-practices.md).

En la lista siguiente se describe cada sección de la documentación del instalador.

-   [Acerca Windows Installer](about-windows-installer.md) proporciona información general sobre las funcionalidades y ventajas del instalador, como anuncios, instalación a petición, resistencia, personalización y administración de componentes. En esta sección se presentan los conceptos de componentes y características del instalador, que son esenciales para comprender cómo el instalador organiza una instalación. También se analizan varios temas de alto nivel sobre la instalación, como la directiva del sistema, las reglas de control de versiones de archivos y la instalación de reversión.
-   [Con Windows Installer](using-windows-installer.md) se tratan diversos temas, como un método estándar para organizar una aplicación en componentes que el instalador puede instalar o quitar del equipo de un usuario; cómo descargar un paquete de instalación desde el World Wide Web; y el uso de imágenes de origen comprimidas.
-   La información de las [secciones What's New in Windows Installer](what-s-new-in-windows-installer.md) (Novedades del instalador de Windows) se puede usar para identificar nuevas características que no son compatibles con versiones anteriores Windows Installer.
-   [Digital Signatures and Windows Installer describe](digital-signatures-and-windows-installer.md) cómo se pueden usar las firmas digitales con paquetes, transformaciones, revisiones, módulos de combinación y archivos de archivado externos.
-   [En Ensamblados](assemblies.md) se explica cómo usar Windows Installer para instalar y administrar el tiempo de ejecución de lenguaje común y los ensamblados win32.
-   [Interfaz de usuario](user-interface.md) proporciona información sobre las funcionalidades de la interfaz de usuario del instalador. Aunque el instalador no proporciona una interfaz de usuario, un autor del paquete puede mantener todos los datos y la lógica necesarios para ejecutar una interfaz de usuario interna o externa totalmente interactiva en la base de datos de instalación. En la sección Referencia se describen los elementos de la interfaz de usuario que se pueden especular en las tablas de base de datos, incluidos los cuadros de diálogo, los controles y los eventos de control.
-   [Acciones estándar](standard-actions.md) describe las acciones estándar que usa el instalador en las tablas de secuencia para realizar una instalación. Esta información está pensada principalmente para desarrolladores de paquetes.
-   [Acciones personalizadas](custom-actions.md) describe cómo crear funcionalidades adicionales en el instalador. Las acciones personalizadas permiten a un autor de un paquete de instalación ampliar las funcionalidades de las acciones estándar mediante la inclusión de archivos ejecutables, bibliotecas de vínculos dinámicos y scripts. Esta información está pensada para desarrolladores de paquetes que necesitan realizar funciones de instalación que no se encuentran en ningún otro lugar del instalador.
-   [Propiedades](properties.md) proporciona información sobre las propiedades que usa el instalador durante una instalación. En las secciones Acerca de y Usar se proporciona información general sobre estas variables globales y cada propiedad se describe en la sección Referencia.
-   [La secuencia de información de resumen](summary-information-stream.md) documenta las propiedades de información de resumen que usa el instalador. Esta información es de interés para todos los desarrolladores.
-   En Revisiones y actualizaciones se describe el uso del instalador para realizar actualizaciones de archivos, ASE, actualizaciones [secundarias,](patching-and-upgrades.md) actualizaciones de productos y revisiones.
-   [Transformaciones](transforms.md) explica cómo modificar o personalizar una base de datos de instalación mediante una transformación de base de datos y cómo generar, proteger y aplicar transformaciones.
-   [La validación de](package-validation.md) paquetes describe el uso de evaluadores de coherencia internos (CIE) para probar la coherencia interna de los paquetes de instalación que están en desarrollo.
-   [Módulos de](merge-modules.md) mezcla presenta un estándar para el diseño de módulos de combinación. Este estándar debe ir seguido de los desarrolladores que crean sus propios módulos de combinación, así como de los desarrolladores que planean usar el instalador para entregar código compartido a sus aplicaciones.
-   Windows Installer en sistemas operativos de [64](windows-installer-on-64-bit-operating-systems.md) bits describe cómo usar Windows Installer para instalar y administrar componentes del instalador diseñados para ejecutarse en sistemas operativos de 64 bits.
-   [Windows ejemplos del](windows-installer-examples.md) instalador incluye un ejemplo paso a paso de la creación de un paquete de instalación con una interfaz de usuario interna en [Un ejemplo de instalación](an-installation-example.md). Para obtener un ejemplo de creación de una actualización principal para un paquete existente, vea [Un ejemplo de actualización](an-upgrade-example.md). Para obtener información sobre cómo una transformación de personalización deshabilita las características y agrega nuevos recursos, vea [Ejemplo de transformación de personalización.](a-customization-transform-example.md) Para obtener un ejemplo de creación de un paquete de revisión que aplica una pequeña actualización a un paquete de instalación existente, vea [A Small Update Patching Example](a-small-update-patching-example.md). Para obtener información sobre cómo encontrar un paquete de instalador existente, vea [Un ejemplo de localización](a-localization-example.md).
-   [Automation Interface](automation-interface.md) proporciona información a los desarrolladores que desean usar la interfaz de automatización de Windows Installer.
-   [Funciones del](installer-functions.md) instalador describe las llamadas de función a la API del instalador. Estas son las funciones a las que llaman otras aplicaciones para acceder a los servicios del instalador para instalar, mantener o quitar aplicaciones. Las secciones Using (Uso) incluyen discusiones sobre cómo solicitar características, iniciar instalaciones y reinstalar los componentes que faltan mediante programación. La sección Referencia es el material de referencia principal para las funciones de servicio del instalador.
-   [Base de datos del instalador](installer-database.md) describe la base de datos de instalación. El instalador conserva toda la lógica y los datos necesarios para una instalación en una base de datos relacional ubicada en un archivo .msi datos. En la sección Acerca de se proporciona información general con diagramas de esquema para los grupos funcionales principales de tablas de la base de datos. En la sección Uso se describe cómo trabajar con el más importante de estas tablas. Estas secciones contienen información esencial para los desarrolladores que están generando paquetes de instalación o escribiendo herramientas de creación de paquetes. La sección Referencia contiene material de referencia completo para cada tabla de base de datos. Esta sección también contiene la referencia principal para cada una de las funciones de base de datos. El instalador usa internamente las funciones de base de datos para acceder a la base de datos y son principalmente de interés para los desarrolladores de herramientas de creación de paquetes del instalador.

 

 



