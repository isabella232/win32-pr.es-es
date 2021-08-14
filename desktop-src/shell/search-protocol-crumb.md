---
description: Comprenda cómo usar el argumento CRUMB en la interfaz de usuario Windows Shell como medio para controlar el ámbito de una búsqueda.
title: Argumento CRUMB (el shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b93764f8014a5d9446811ef622f7c5afc20acbc6193d938c98642afaae5392fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452881"
---
# <a name="crumb-argument-the-windows-shell"></a>Argumento CRUMB (el shell Windows)

El argumento admite instrucciones de sintaxis de consulta avanzada (AQS) completa y es especialmente útil como medio para controlar el `crumb` ámbito de una búsqueda. Además de las instrucciones de AQS, el argumento puede tomar un parámetro especial en Windows Vista y los parámetros y en Windows XP, como se describe más adelante `crumb` `location` en este `kind` `store` tema.

Este tema contiene las siguientes secciones:

-   [Sintaxis de miga](#crumb-syntax)
    -   [Ejemplos generales](#general-examples)
-   [Uso de miga con Vista (ubicación)](#using-crumb-with-vista-location)
    -   [Ejemplos de Vista](#vista-examples)
    -   [Constantes para carpetas comunes](#constants-for-common-folders)
    -   [Información de argumentos](#argument-information)

## <a name="crumb-syntax"></a>Sintaxis de miga

La sintaxis de la miga es la siguiente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte es cualquier propiedad del sistema de propiedades y <value> portion es un valor válido para esa propiedad. La <label> parte es un alias opcional para la propiedad que se muestra como una sugerencia de interfaz de usuario.

### <a name="general-examples"></a>Ejemplos generales


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Uso de miga con Vista (ubicación)

En el parámetro crumb, Windows Vista admite AQS completo y también la propiedad , que tiene una implementación especial disponible solo `location` en Windows Vista. Puede usar una cadena de AQS o la propiedad `location` dentro de un único parámetro crumb, pero no ambos. Si el parámetro crumb incluye AQS, se omite todo lo demás de ese parámetro de miga.

La `location` propiedad permite especificar una ruta de acceso para buscar. Windows Vista puede omitir el indexador y atravesar el directorio directamente si la ubicación está fuera del ámbito de rastreo del indexador. Por lo tanto, estas búsquedas pueden ser más lentas que las búsquedas que usan el indexador.

Cuando se especifica una `location` propiedad, se admiten dos parámetros adicionales y opcionales:



| Parámetro | Valores                  | Descripción                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserción | include, exclude        | Especifica si la consulta debe incluir o excluir elementos de esa ruta de acceso. "Include" es el valor predeterminado. Windows Vista no admite exclusiones sin inclusiones. (Vea el ejemplo) |
| recursión | recursiva, no recursiva | Especifica si la búsqueda debe repetir todas las subcarpetas a partir del valor definido en la ubicación:<value>. "Recursive" es el valor predeterminado.                             |



 

Para el ámbito de una búsqueda mediante el protocolo **search:** , tiene distintas opciones en función del destino del ámbito.

Carpeta en un equipo local:

-   Usar AQS (crumb=folder:<ruta de acceso con codificación URL>)
-   Uso del argumento location (crumb=location:<ruta de acceso codificada con url>)

Carpeta en una máquina o red remota:

-   Uso del argumento location (crumb=location:<ruta de acceso codificada con url>)

Carpeta a la que se accede a través de un controlador de protocolo conocido de convención de nomenclatura universal (UNC):

-   Use AQS (crumb=store: <UNC protocol handler name> )
-   Uso del argumento location (crumb=location:<ruta de acceso codificada con url>)

### <a name="vista-examples"></a>Ejemplos de Vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



En el primer ejemplo se ejecuta una búsqueda de "vacaciones" a partir de la ubicación (un acceso directo especial a la carpeta Mis documentos del usuario), incluida esa carpeta y todas las `shell://Personal` subcarpetas.  Consulte la tabla siguiente.

En el segundo ejemplo se ejecuta una búsqueda en C: \\ Imágenes, pero no en C: \\ Imágenes \\ duplicadas.

En el tercer ejemplo se ejecuta una búsqueda en C: Documentos, limitada a archivos con \\ la propiedad establecida en `kind` imágenes.

### <a name="constants-for-common-folders"></a>Constantes para carpetas comunes

Windows Vista permite el uso de valores CSIDL que proporcionan una manera única independiente del sistema de identificar carpetas especiales usadas con frecuencia por las aplicaciones, pero que pueden no tener el mismo nombre o ubicación en un sistema determinado. Por ejemplo, la carpeta del sistema puede ser "C: Windows" en un sistema y \\ "C: \\ Winnt" en otro.

Use estas ubicaciones con esta sintaxis:


```
crumb=location:shell%3a<LocationName>&
```



En la tabla siguiente se enumeran los valores de CSIDL. Consulte [**ShellSpecialFolderConstants para**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) obtener más información.



| Nombre                        | cadena de búsqueda                   | Descripción                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HERRAMIENTAS ADMINISTRATIVAS        | ADMINISTRATIVE%20TOOLS          | Directorio del sistema de archivos que actúa como repositorio para herramientas administrativas.                                                                                                            |
| APPDATA                     | APPDATA                         | Directorio del sistema de archivos que actúa como repositorio común para datos específicos de la aplicación. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario Datos de \\ \\ aplicación.                      |
| CACHE                       | CACHE                           | Directorio del sistema de archivos que actúa como repositorio común para archivos temporales de Internet. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario Archivos temporales de \\ \\ Internet.               |
| CD DESALMACIÓN                  | CD%20SERCIÓN                    | Carpeta que contiene los datos que se va a convertir en CD.                                                                                                                                             |
| HERRAMIENTAS ADMINISTRATIVAS COMUNES | COMMON%20ADMINISTRATIVE%20TOOLS | Herramientas administrativas para todos los usuarios.                                                                                                                                                    |
| COMMON APPDATA              | COMMON%20APPDATA                | Datos de aplicación para todos los usuarios. Una ruta de acceso típica es C: \\ Documentos y Configuración de la aplicación Todos los \\ \\ usuarios.                                                                             |
| ESCRITORIO COMÚN              | ESCRITORIO COMÚN                  | Microsoft Windows Desktop para todos los usuarios. Carpeta virtual que es la raíz del espacio de nombres.                                                                                        |
| DOCUMENTOS COMUNES            | COMMON%20DOCUMENTS              | Documentos para todos los usuarios. Una ruta de acceso típica es C: \\ Documentos y Configuración Todos los usuarios \\ \\ Mis documentos.                                                                                        |
| PROGRAMAS COMUNES             | COMMON%20PROGRAMS               | Grupos de programas comunes a todos los usuarios. Una ruta de acceso típica es C: \\ Documentos y Configuración programas de menú Inicio de todos los \\ \\ \\ usuarios.                                                                     |
| MENÚ INICIO COMÚN           | COMMON%20START%20MENU           | menú Inicio elementos comunes a todos los usuarios. Una ruta de acceso típica es C: \\ Documentos y Configuración Menú Inicio de todos los \\ \\ usuarios.                                                                             |
| INICIO COMÚN              | COMMON%20STARTUP                | Grupo de programas de inicio común a todos los usuarios.                                                                                                                                             |
| PLANTILLAS COMUNES            | COMMON%20TEMPLATES              | Plantillas de documento comunes a todos los usuarios.                                                                                                                                                |
| COMMONMUSIC                 | MY%20 RESALTE                      | Mis Música carpetas comunes a todos los usuarios.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | Plantillas de carpeta Mis imágenes comunes a todos los usuarios.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Las plantillas de carpeta Mi vídeo son comunes a todos los usuarios.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | carpeta que contiene los datos de conexión.                                                                                                                                                     |
| CARPETA DEL PANEL DE CONTROL        | CONTROLPANELFOLDER              | Carpeta virtual que contiene iconos para las Panel de control virtuales.                                                                                                                    |
| Galletas                     | Galletas                         | Directorio del sistema de archivos que actúa como repositorio común para las cookies de Internet. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario \\ \\ Cookies.                                        |
| ESCRITORIO                     | ESCRITORIO                         | Microsoft Windows Desktop. Carpeta virtual que es la raíz del espacio de nombres.                                                                                                           |
| FAVORITOS                   | FAVORITOS                       | Directorio del sistema de archivos que actúa como repositorio común para los elementos favoritos del usuario. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario \\ \\ Favoritos.                             |
| Fuentes                       | Fuentes                           | Carpeta virtual que contiene fuentes instaladas. Una ruta de acceso típica es C: \\ Fuentes \\ WINDOWS.                                                                                                       |
| HISTORIAL                     | HISTORIAL                         | Directorio del sistema de archivos que actúa como repositorio común para los elementos del historial de Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Carpeta que contiene datos de Internet.                                                                                                                                                    |
| LOCAL APPDATA               | LOCAL%20APPDATA                 | Directorio del sistema de archivos que actúa como repositorio de datos para aplicaciones locales (no móviles). Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario Local Configuración Application \\ \\ \\ Data. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Directorio de recursos localizado.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Mi PC. Carpeta virtual que contiene todo el contenido del equipo local: dispositivos de almacenamiento, impresoras y Panel de control. Esta carpeta también puede contener unidades de red asignadas.             |
| MI MÚSICA                    | MY%20 RESALTE                      | Mi Música carpeta. Una ruta de acceso típica es C: \\ Documents and Configuración username Mis documentos My \\ \\ \\ Música.                                                                                       |
| MIS IMÁGENES                 | MY%20PICTURES                   | Carpeta Mis imágenes. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre Mis documentos Mis \\ \\ \\ imágenes.                                                                                 |
| MI VÍDEO                    | MY%20VIDEO                      | Carpeta Mi vídeo. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre Mis documentos Mi \\ \\ \\ vídeo.                                                                                       |
| NET ESTANDO EN LA RED                     | NET ESTANDO EN LA RED                         | Carpeta virtual que representa la raíz de la jerarquía de espacios de nombres de red.                                                                                                               |
| CARPETA NETWORK PLACES       | NETWORKDPLACESFOLDER            | Carpeta del sistema de archivos que contiene los objetos de vínculo que pueden existir en la carpeta virtual Mis lugares de red. No es lo mismo que NET NAMESPACE, que representa la raíz del espacio de nombres de red.   |
| VÍNCULOS DE OEM                   | OEM%20LINKS                     | Carpeta que contiene vínculos a sitios de OEM.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Directorio del sistema de archivos que actúa como repositorio común para los documentos de un usuario. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre \\ \\ Mis documentos.                                 |
| CARPETA IMPRESORAS             | CARPETA IMPRESORAS                 | Carpeta virtual que contiene impresoras instaladas.                                                                                                                                          |
| PRINT RESALTE                   | PRINT RESALTE                       | Directorio del sistema de archivos que contiene los objetos de vínculo que pueden existir en la carpeta virtual Impresoras. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario Print \\ \\ Resalte.                 |
| PROGRAMAS                    | PROGRAMAS                        | Directorio del sistema de archivos que contiene los grupos de programas del usuario (que también son directorios del sistema de archivos). Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario Programas de menú \\ \\ \\ Inicio.  |
| PROFILE                     | PROFILE                         | Carpeta de perfil del usuario.                                                                                                                                                                 |
| ARCHIVOS DE PROGRAMA               | PROGRAM%20FILES                 | Carpeta Archivos de programa. Una ruta de acceso típica es C: \\ Archivos de programa.                                                                                                                             |
| ARCHIVOS DE PROGRAMA COMUNES        | PROGRAMFILESCOMMON              | Carpeta Archivos de programa común a todos los usuarios.                                                                                                                                              |
| ARCHIVOS DE PROGRAMA COMUNES X86    | PROGRAMFILESCOMMONX86           | Carpeta Archivos de programa común a todos los usuarios de máquinas x86.                                                                                                                              |
| ARCHIVOS DE PROGRAMAX86            | PROGRAMFILESx86                 | Carpeta Archivos de programa en máquinas x86.                                                                                                                                                  |
| Reciente                      | Reciente                          | Directorio del sistema de archivos que contiene los documentos usados más recientemente del usuario. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario \\ \\ Reciente.                                           |
| CARPETA PAPELERA DE RECICLAJE          | RECYCLEBINFOLDER                | Carpeta virtual que contiene los objetos de la cuenta del papelera de reciclaje.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Directorio de recursos.                                                                                                                                                                |
| Sendto                      | Sendto                          | Directorio del sistema de archivos que contiene elementos de menú Enviar a. Una ruta de acceso típica es C: \\ Documentos y Configuración nombre de usuario \\ \\ SendTo.                                                                |
| MENÚ INICIO                  | START%20MENU                    | Directorio del sistema de archivos que menú Inicio elementos. Una ruta de acceso típica es C: \\ Documents and Configuración username Start Menu (C: documentos y nombre de \\ \\ usuario).                                                                 |
| Inicio                     | Inicio                         | Directorio del sistema de archivos que corresponde al grupo de programas De inicio del usuario.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Carpeta del sistema en máquinas x86.                                                                                                                                                         |
| PLANTILLAS                   | PLANTILLAS                       | Directorio del sistema de archivos que actúa como repositorio común para las plantillas de documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Carpeta del sistema. Una ruta de acceso típica es C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows directorio o SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Información de argumentos



|                              | Value                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo mínimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



