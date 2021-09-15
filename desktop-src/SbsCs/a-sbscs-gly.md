---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271831"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (aplicaciones aisladas y ensamblados en paralelo)

A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexto de activación**
</dt> <dd>

Estructura de datos en memoria. Cada sección de esta estructura contiene metadatos para las funciones de API en paralelo. Por ejemplo, una sección puede tener datos de redireccionamiento de DLL, que usa el cargador de DLL, y otra puede tener datos de servidor COM. Estos datos se pueden usar para redirigir la carga de un archivo DLL a una versión específica, la creación de un objeto COM o la creación de una ventana a una versión más compatible con la aplicación.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuración de la aplicación**
</dt> <dd>

Nombres y versiones de ensamblados en paralelo necesarios para ejecutar una aplicación. Cuando se implementa una aplicación con un manifiesto, se definen explícitamente las dependencias de versiones específicas de ensamblados compartidos en paralelo. De forma predeterminada, la versión del ensamblado especificado en el manifiesto es la versión que se usa tras la activación. La configuración global de la aplicación especifica la configuración de todas las aplicaciones del sistema. La configuración por aplicación puede invalidar la configuración global de la aplicación por aplicación.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifiesto de configuración de la aplicación**
</dt> <dd>

Archivo que especifica los ensamblados en paralelo que va a usar una aplicación completamente o parcialmente aislada. Los archivos de manifiesto de configuración de la aplicación se instalan en la misma carpeta que el archivo ejecutable de la aplicación.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifiesto de aplicación**
</dt> <dd>

Archivo que describe una aplicación aislada. Especifica la información necesaria para ejecutar la aplicación, incluidas las dependencias de ensamblados privados, versiones específicas de ensamblados compartidos y metadatos para ensamblados privados. El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de la extensión .manifest. Por ejemplo, para MySampleApp.exe, el archivo de manifiesto se MySampleApp.exe.manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**ensamblaje**
</dt> <dd>

Unidad fundamental para asignar nombres, enlazar, control de versiones, implementar o configurar un bloque de código de programación. Estos ensamblados de código se pueden colocar en archivos DLL o ensamblados COM. Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación que se conocen como módulos o ensamblados de código. La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifiesto de ensamblado**
</dt> <dd>

Descripción de un ensamblado en paralelo. Especifica el nombre, la versión, los archivos, los recursos del ensamblado, los datos de enlace de los elementos del ensamblado y las dependencias de otros ensamblados en paralelo. Un archivo de manifiesto de ensamblado puede tener cualquier nombre de archivo válido, siempre que esté seguido de la extensión .manifest.

</dd> </dl>

 

 



