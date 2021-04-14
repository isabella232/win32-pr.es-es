---
description: El argumento migas admite instrucciones completas de sintaxis de consulta avanzada (AQS) y es especialmente útil como medio para controlar el ámbito de una búsqueda.
title: Argumento de MIGAs (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7d38fff38c14a6b537bde068b92e19cedf53d5d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985759"
---
# <a name="crumb-argument-the-windows-shell"></a>Argumento de MIGAs (Shell de Windows)

El `crumb` argumento admite instrucciones completas de sintaxis de consulta avanzada (AQS) y es especialmente útil como medio para controlar el ámbito de una búsqueda. Además de las instrucciones de AQS, el `crumb` argumento puede tomar un `location` parámetro especial en Windows Vista `kind` y `store` los parámetros de Windows XP, tal y como se describe más adelante en este tema.

Este tema contiene las siguientes secciones:

-   [Sintaxis de migas](#crumb-syntax)
    -   [Ejemplos generales](#general-examples)
-   [Uso de migas de vista (ubicación)](#using-crumb-with-vista-location)
    -   [Ejemplos de vista](#vista-examples)
    -   [Constantes para carpetas comunes](#constants-for-common-folders)
    -   [Información de argumentos](#argument-information)

## <a name="crumb-syntax"></a>Sintaxis de migas

La sintaxis de las rutas de navegación es la siguiente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte es cualquier propiedad del sistema de propiedades y el <value> la parte es un valor válido para esa propiedad. La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.

### <a name="general-examples"></a>Ejemplos generales


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Uso de migas de vista (ubicación)

En el parámetro de rutas de acceso, Windows Vista admite AQS completo y también la `location` propiedad, que tiene una implementación especial disponible solo en Windows Vista. Puede usar una cadena AQS o la `location` propiedad dentro de un único parámetro de migas de línea, pero no ambos. Si el parámetro de migas incluye AQS, se omite todo lo demás en ese parámetro de migas de detalle.

La `location` propiedad permite especificar una ruta de acceso que se va a buscar. Windows Vista puede omitir el indexador y atravesar el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador. Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.

Cuando se especifica una `location` propiedad, se admiten dos parámetros adicionales y son opcionales:



| Parámetro | Valores                  | Descripción                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Introducción | incluir, excluir        | Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso. "Include" es el valor predeterminado. Windows Vista no admite exclusiones sin inclusiones. (Vea el ejemplo) |
| recursión | recursivo, no recursiva | Especifica si la búsqueda debe recurse todas las subcarpetas a partir del valor definido en la ubicación:<value>. "Recursive" es el valor predeterminado.                             |



 

Para establecer el ámbito de una búsqueda mediante el protocolo **Search:** , tiene distintas opciones según el destino del ámbito.

En una máquina local:

-   Usar AQS (migas = carpeta: <ruta de acceso con codificación URL>)
-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

Carpeta en un equipo o red remoto:

-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

Carpeta a la que se obtiene acceso a través de un controlador de protocolo de Convención de nomenclatura universal (UNC) conocido:

-   Usar AQS (migas de la tienda: <UNC protocol handler name> )
-   Use el argumento de ubicación (migas de Ubicación: <ruta de acceso con codificación URL>)

### <a name="vista-examples"></a>Ejemplos de vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la `shell://Personal` Ubicación (un acceso directo especial a la carpeta **Mis documentos** del usuario), incluida la carpeta y todas las subcarpetas. Consulte la tabla siguiente.

En el segundo ejemplo se ejecuta una búsqueda dentro de C: \\ Pictures, pero no en c: \\ imágenes \\ duplicadas.

En el tercer ejemplo se ejecuta una búsqueda en C: \\ Documents, limitada a los archivos con la `kind` propiedad establecida en pics.

### <a name="constants-for-common-folders"></a>Constantes para carpetas comunes

Windows Vista permite el uso de valores de CSIDL que proporcionan una manera única independiente del sistema para identificar carpetas especiales usadas con frecuencia por aplicaciones, pero que pueden no tener el mismo nombre o ubicación en ningún sistema determinado. Por ejemplo, la carpeta del sistema puede ser "C: \\ Windows" en un sistema y "c: \\ WinNT" en otro.

Use estas ubicaciones con esta sintaxis:


```
crumb=location:shell%3a<LocationName>&
```



En la tabla siguiente se enumeran los valores de CSIDL. Consulte [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para obtener más información.



| Nombre                        | cadena de búsqueda                   | Descripción                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HERRAMIENTAS ADMINISTRATIVAS        | % 20TOOLS ADMINISTRATIVO          | Directorio del sistema de archivos que actúa como repositorio de herramientas administrativas.                                                                                                            |
| APPDATA                     | APPDATA                         | Directorio del sistema de archivos que sirve de repositorio común para los datos específicos de la aplicación. Una ruta de acceso típica es C: \\ Documents and Settings \\ username \\ Application Data.                      |
| CACHE                       | CACHE                           | Directorio del sistema de archivos que sirve de repositorio común para los archivos temporales de Internet. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombre de usuario \\ archivos temporales de Internet.               |
| GRABACIÓN DE CD                  | CD% 20BURNING                    | Carpeta que contiene los datos que se van a grabar en el CD.                                                                                                                                             |
| HERRAMIENTAS ADMINISTRATIVAS COMUNES | % 20ADMINISTRATIVE% 20TOOLS COMÚN | Herramientas administrativas para todos los usuarios.                                                                                                                                                    |
| APPDATA COMUNES              | % 20APPDATA COMUNES                | Datos de aplicación para todos los usuarios. Una ruta de acceso típica es C: \\ Documents and Settings \\ All Users \\ Application Data.                                                                             |
| ESCRITORIO COMÚN              | ESCRITORIO COMÚN                  | Datos del escritorio de Microsoft Windows para todos los usuarios. Carpeta virtual que es la raíz del espacio de nombres.                                                                                        |
| DOCUMENTOS COMUNES            | % 20DOCUMENTS COMUNES              | Documentos para todos los usuarios. Una ruta de acceso típica es C: \\ Documents and Settings \\ All Users \\ Mis documentos.                                                                                        |
| PROGRAMAS COMUNES             | % 20PROGRAMS COMUNES               | Grupos de programas comunes a todos los usuarios. Una ruta de acceso típica es C: \\ Documents and Settings \\ All Users \\ Start Menu \\ programs.                                                                     |
| MENÚ INICIO COMÚN           | % 20START% 20MENU COMÚN           | Elementos del menú Inicio comunes a todos los usuarios. Una ruta de acceso típica es C: \\ Documents and Settings \\ todos los usuarios \\ menú Inicio.                                                                             |
| INICIO COMÚN              | % 20STARTUP COMUNES                | Grupo de programas de inicio común a todos los usuarios.                                                                                                                                             |
| PLANTILLAS COMUNES            | % 20TEMPLATES COMUNES              | Plantillas de documentos comunes a todos los usuarios.                                                                                                                                                |
| COMMONMUSIC                 | MI% 20MUSIC                      | Mis plantillas de carpeta música comunes a todos los usuarios.                                                                                                                                         |
| COMMONPICTURES              | MI% 20PICTURES                   | Mis imágenes plantillas de carpeta comunes a todos los usuarios.                                                                                                                                      |
| COMMONVIDEO                 | MI% 20VIDEO                      | Mis plantillas de carpeta de vídeo comunes a todos los usuarios.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | carpeta que contiene los datos de conexión.                                                                                                                                                     |
| CARPETA DEL PANEL DE CONTROL        | CONTROLPANELFOLDER              | Carpeta virtual que contiene iconos para las aplicaciones del panel de control.                                                                                                                    |
| PROPIAS                     | PROPIAS                         | Directorio del sistema de archivos que sirve de repositorio común para las cookies de Internet. Una ruta de acceso típica es C: \\ Documents and Settings \\ username \\ cookies.                                        |
| ESCRITORIO                     | ESCRITORIO                         | Escritorio de Microsoft Windows. Carpeta virtual que es la raíz del espacio de nombres.                                                                                                           |
| FAVORITOS                   | FAVORITOS                       | Directorio del sistema de archivos que sirve de repositorio común para los elementos favoritos del usuario. Una ruta de acceso típica es C: \\ Documents and Settings \\ username \\ Favorites.                             |
| ÉSTAS                       | ÉSTAS                           | Carpeta virtual que contiene las fuentes instaladas. Una ruta de acceso típica es C: \\ fuentes de Windows \\ .                                                                                                       |
| HISTORIAL                     | HISTORIAL                         | Directorio del sistema de archivos que sirve de repositorio común para los elementos del historial de Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Carpeta que contiene datos de Internet.                                                                                                                                                    |
| APPDATA LOCALES               | % 20APPDATA LOCAL                 | Directorio del sistema de archivos que actúa como repositorio de datos para aplicaciones locales (no móviles). Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ configuración regional \\ Data. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Directorio de recursos localizado.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Mi PC. Carpeta virtual que contiene todo el contenido del equipo local: dispositivos de almacenamiento, impresoras y panel de control. Esta carpeta también puede contener unidades de red asignadas.             |
| MI MÚSICA                    | MI% 20MUSIC                      | Carpeta mi música. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ My mis documentos \\ mi música.                                                                                       |
| MIS IMÁGENES                 | MI% 20PICTURES                   | Carpeta Mis imágenes. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ Mis documentos \\ Mis imágenes.                                                                                 |
| MI VÍDEO                    | MI% 20VIDEO                      | Carpeta mi vídeo. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ Mis documentos \\ mi vídeo.                                                                                       |
| NETHOOD                     | NETHOOD                         | Carpeta virtual que representa la raíz de la jerarquía de espacios de nombres de red.                                                                                                               |
| CARPETA DE SITIOS DE RED       | NETWORKDPLACESFOLDER            | Carpeta del sistema de archivos que contiene los objetos de vínculo que pueden existir en la carpeta virtual mis sitios de red. No es lo mismo que NETHOOD, que representa la raíz del espacio de nombres de red.   |
| VÍNCULOS DE OEM                   | % 20LINKS OEM                     | Carpeta que contiene vínculos a sitios OEM.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Directorio del sistema de archivos que sirve de repositorio común para los documentos de un usuario. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ Mis documentos.                                 |
| CARPETA IMPRESORAS             | CARPETA IMPRESORAS                 | Carpeta virtual que contiene las impresoras instaladas.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Directorio del sistema de archivos que contiene los objetos de vínculo que pueden existir en la carpeta virtual impresoras. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ PrintHood.                 |
| PROGRAMAS                    | PROGRAMAS                        | Directorio del sistema de archivos que contiene los grupos de programas del usuario (que también son directorios del sistema de archivos). Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ Inicio menú \\ programas.  |
| PROFILE                     | PROFILE                         | Carpeta de perfil del usuario.                                                                                                                                                                 |
| ARCHIVOS DE PROGRAMA               | PROGRAMA% 20FILES                 | Carpeta archivos de programa. Una ruta de acceso típica es C: \\ archivos de programa.                                                                                                                             |
| ARCHIVOS DE PROGRAMA COMUNES        | PROGRAMFILESCOMMON              | Carpeta de archivos de programa común para todos los usuarios.                                                                                                                                              |
| ARCHIVOS de programa comunes x86    | PROGRAMFILESCOMMONX86           | Carpeta de archivos de programa común para todos los usuarios en equipos x86.                                                                                                                              |
| Programa FILESx86            | PROGRAMFILESx86                 | Carpeta archivos de programa en equipos x86.                                                                                                                                                  |
| ÚLTIMO                      | ÚLTIMO                          | Directorio del sistema de archivos que contiene los documentos usados más recientemente del usuario. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ reciente.                                           |
| CARPETA DE LA PAPELERA DE RECICLAJE          | RECYCLEBINFOLDER                | Carpeta virtual que contiene los objetos de la papelera de reciclaje del usuario.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | El directorio de recursos.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Directorio del sistema de archivos que contiene los elementos de menú enviar a. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ SendTo.                                                                |
| MENÚ INICIO                  | INICIAR% 20MENU                    | Directorio del sistema de archivos que contiene los elementos del menú Inicio. Una ruta de acceso típica es C: \\ Documents and Settings \\ nombreDeUsuario \\ Inicio menu.                                                                 |
| Inicio                     | Inicio                         | Directorio del sistema de archivos que corresponde al grupo de programas de inicio del usuario.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Carpeta del sistema en equipos x86.                                                                                                                                                         |
| PLANTILLAS                   | PLANTILLAS                       | Directorio del sistema de archivos que sirve de repositorio común para plantillas de documentos.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Carpeta del sistema. Una ruta de acceso típica es C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Directorio de Windows o SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Información de argumentos



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo mínimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



