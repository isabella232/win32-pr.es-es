---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687430"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (aplicaciones aisladas y ensamblados en paralelo)

A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N o [p](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [s](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexto de activación**
</dt> <dd>

Estructura de datos en memoria. Cada sección de esta estructura contiene metadatos para las funciones de la API que están en paralelo. Por ejemplo, una sección puede tener datos de redireccionamiento de DLL, que usa el cargador de DLL, y otro puede tener datos de servidor COM. Estos datos se pueden usar para redirigir la carga de una DLL a una versión concreta, la creación de un objeto COM o la creación de una ventana en una versión que sea más compatible para la aplicación.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuración de la aplicación**
</dt> <dd>

Nombres y versiones de los ensamblados en paralelo necesarios para ejecutar una aplicación. Cuando una aplicación se implementa con un manifiesto, se definen explícitamente las dependencias de las versiones específicas de los ensamblados en paralelo compartidos. De forma predeterminada, la versión del ensamblado especificado en el manifiesto es la versión que se usa durante la activación. La configuración global de la aplicación especifica la configuración de todas las aplicaciones del sistema. La configuración por aplicación puede invalidar la configuración global de la aplicación por aplicación.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifiesto de configuración de la aplicación**
</dt> <dd>

Archivo que especifica los ensamblados en paralelo que se van a usar en una aplicación totalmente o parcialmente aislada. Los archivos de manifiesto de configuración de la aplicación se instalan en la misma carpeta que el archivo ejecutable de la aplicación.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifiesto de aplicación**
</dt> <dd>

Archivo que describe una aplicación aislada. Especifica la información necesaria para ejecutar la aplicación, incluidas las dependencias de ensamblados privados, las versiones específicas de los ensamblados y metadatos compartidos para los ensamblados privados. El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de la extensión. manifest. Por ejemplo, para MySampleApp.exe, el archivo de manifiesto sería MySampleApp.exe. manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembl**
</dt> <dd>

Unidad fundamental para la nomenclatura, el enlace, el control de versiones, la implementación o la configuración de un bloque de código de programación. Estos ensamblados de código se pueden colocar en archivos dll o ensamblados COM. Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación a los que se hace referencia como módulos o ensamblados de código. La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifiesto del ensamblado**
</dt> <dd>

Descripción de un ensamblado en paralelo. Especifica el nombre, la versión, los archivos, los recursos del ensamblado, los datos de enlace para los elementos del ensamblado y las dependencias de otros ensamblados en paralelo. Un archivo de manifiesto del ensamblado puede tener cualquier nombre de archivo válido, siempre y cuando vaya seguido del manifiesto de la extensión. manifest.

</dd> </dl>

 

 



