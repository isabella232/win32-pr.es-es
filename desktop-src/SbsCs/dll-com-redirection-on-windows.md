---
description: El redireccionamiento de DLL/COM es una estrategia de aislamiento de aplicaciones que emplean los administradores corporativos Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Redirección de DLL/COM en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ce6b55c2a66d298b7b80248613eab7cefe96c25f8f53dd9218966e235ea267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142268"
---
# <a name="dllcom-redirection-on-windows"></a>Redirección de DLL/COM en Windows

El redireccionamiento de DLL/COM es una estrategia de aislamiento de aplicaciones que emplean los administradores corporativos Windows XP.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP con SP2: ** No se recomienda el uso de estrategias de redirección de DLL/COM porque las aplicaciones aisladas que usan manifiestos y ensamblados en paralelo pueden ser más [fáciles](about-side-by-side-assemblies-.md) de actualizar y dar servicio. La presencia de un archivo .local se omite si hay un manifiesto. La estrategia de redirección de DLL/COM que usa archivos .local funciona si la aplicación no tiene un manifiesto.

El redireccionamiento de DLL/COM enlaza una aplicación a una versión local de un componente. Los archivos del componente local se pueden mantener separados de la versión del sistema del componente en una ubicación privada para la aplicación. La versión del componente del sistema se registra globalmente y está disponible para cualquier otra aplicación que se enlaza a él. La versión local del componente está reservada para el uso exclusivo de la aplicación. Si es necesario, los archivos de componente utilizados por la aplicación se pueden cargar en la memoria al mismo tiempo que los archivos de componentes del sistema.

La redirección de DLL/COM se activa instalando un archivo especial junto con una copia del archivo de componente local en el mismo directorio que el archivo ejecutable de la aplicación. El archivo especial es un archivo vacío denominado después del nombre del archivo ejecutable de la aplicación y anexado a .local. Por ejemplo, para activar el redireccionamiento DE DLL/COM para una aplicación denominada Myapp, la versión local del componente y un archivo vacío denominado Myapp.exe.local deben copiarse en la carpeta que contiene Myapp.exe. Esto enlaza la aplicación a la versión local del componente en lugar de a la versión compartida globalmente del componente.

Cuando una aplicación carga un archivo de componente, como un archivo DLL o .ocx, Windows lo busca primero en la carpeta donde está instalado el archivo .local y ejecutable de la aplicación. Si se encuentra, la aplicación usa ese archivo de componente independientemente de cualquier ruta de acceso de búsqueda de directorio definida en la aplicación o el Registro. Si no se encuentra, se usa el archivo de componente en la ruta de acceso de búsqueda definida.

La utilidad de instalación debe hacer lo siguiente para instalar la aplicación con redirección de DLL/COM:

-   Un archivo .local vacío debe copiarse en la misma carpeta que el archivo ejecutable de la aplicación.
-   Todos los componentes, dll y archivos .ocx usados por la aplicación deben copiarse en la misma carpeta que el archivo ejecutable de la aplicación.
-   Los componentes COM aislados deben registrarse con Windows para que las distintas versiones del ensamblado no entren en conflicto entre sí cuando se cargan en la memoria al mismo tiempo. El proceso de registro requiere que, aunque la implementación del componente pueda cambiar entre versiones, determinados metadatos COM como CLSID, ProgID, Biblioteca de tipos y Modelo de subprocesos no puedan.
-   Si la aplicación se instala mediante el instalador Windows, el directorio de la aplicación se puede proteger mediante la tabla LockPermissions. Normalmente, al sistema se le proporciona acceso de lectura, escritura y ejecución. a todos los demás procesos solo se les proporciona acceso de ejecución y lectura.

 

 



