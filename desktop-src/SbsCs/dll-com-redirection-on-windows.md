---
description: La redirección de DLL/COM es una estrategia de aislamiento de aplicaciones empleada por los administradores corporativos en Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Redirección de DLL/COM en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911886"
---
# <a name="dllcom-redirection-on-windows"></a>Redirección de DLL/COM en Windows

La redirección de DLL/COM es una estrategia de aislamiento de aplicaciones empleada por los administradores corporativos en Windows XP.

* * Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP con SP2: * * no se recomienda el uso de las estrategias de redirección de DLL/COM porque las aplicaciones aisladas que usan manifiestos y [ensamblados en paralelo](about-side-by-side-assemblies-.md) pueden ser más fáciles de actualizar y de atender. La presencia de un archivo. local se omite si existe un manifiesto. La estrategia de redirección de DLL/COM mediante archivos. local funciona si la aplicación no tiene un manifiesto.

La redirección COM/DLL enlaza una aplicación a una versión local de un componente. Los archivos del componente local se pueden mantener separados de la versión del sistema del componente en una ubicación que sea privada para la aplicación. La versión del sistema del componente se registra globalmente y está disponible para cualquier otra aplicación que se enlaza a él. La versión local del componente está reservada para el uso exclusivo de la aplicación. Si es necesario, los archivos de componentes usados por la aplicación se pueden cargar en la memoria al mismo tiempo que los archivos de componentes del sistema.

La redirección de DLL/COM se activa instalando un archivo especial junto con una copia del archivo de componente local en el mismo directorio que el archivo ejecutable de la aplicación. El archivo especial es un archivo vacío denominado después del nombre de archivo del ejecutable de la aplicación y se ha anexado con. local. Por ejemplo, para activar el redireccionamiento de DLL/COM para una aplicación denominada MyApp, la versión local del componente y un archivo vacío denominado Myapp.exe. local deben copiarse en la carpeta que contiene Myapp.exe. Esto enlaza la aplicación a la versión local del componente en lugar de a la versión compartida globalmente del componente.

Cuando una aplicación carga un archivo de componente, como un archivo DLL o. ocx, Windows busca primero en la carpeta donde está instalado el archivo. local y el ejecutable de la aplicación. Si se encuentra, la aplicación usa ese archivo de componente independientemente de la ruta de acceso de búsqueda de directorio definida en la aplicación o en el registro. Si no se encuentra, se utiliza el archivo de componente de la ruta de búsqueda definida.

La utilidad de instalación debe hacer lo siguiente para instalar la aplicación con redireccionamiento de DLL/COM:

-   Un archivo. local vacío debe copiarse en la misma carpeta que el archivo ejecutable de la aplicación.
-   Todos los componentes, DLL y archivos. ocx usados por la aplicación deben copiarse en la misma carpeta que el archivo ejecutable de la aplicación.
-   Los componentes COM aislados se deben registrar en Windows para que las distintas versiones del ensamblado no entren en conflicto entre sí cuando se cargan en la memoria al mismo tiempo. El proceso de registro requiere que, mientras que la implementación del componente puede cambiar entre versiones, ciertos metadatos COM como CLSID, ProgID, biblioteca de tipos y el modelo de subprocesos no pueden.
-   Si la aplicación se instala mediante el Windows Installer, el directorio de la aplicación se puede proteger mediante la tabla LockPermissions. Normalmente, el sistema recibe acceso de lectura, escritura y ejecución. a todos los demás procesos solo se les proporciona acceso de ejecución y de lectura.

 

 



