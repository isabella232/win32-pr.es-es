---
description: La creación de una aplicación habilitada para ejecución automática es un procedimiento sencillo. En este tema se usa CD-ROM como ejemplo (fue el primer medio en implementar esta tecnología), pero actualmente hay muchos tipos de medios diferentes que pueden usarlo.
title: Creación de una AutoRun-Enabled aplicación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f3a3c265f71b0bdf66d7825e65eb69ab975bfc6bffa5c9a8674ed5a0fb8feb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224937"
---
# <a name="creating-an-autorun-enabled-application"></a>Creación de una AutoRun-Enabled aplicación

La creación de una aplicación habilitada para ejecución automática es un procedimiento sencillo. En este tema se usa CD-ROM como ejemplo (fue el primer medio en implementar esta tecnología), pero actualmente hay muchos tipos de medios diferentes que pueden usarlo.

Para habilitar AutoRun en la aplicación, basta con incluir dos archivos esenciales:

-   Un archivo Autorun.inf
-   Una aplicación de inicio

Cuando un usuario inserta un disco en una unidad de CD-ROM en un equipo compatible con AutoRun, el sistema comprueba inmediatamente si el disco tiene un sistema de archivos de equipo personal. Si es así, el sistema busca un archivo denominado [Autorun.inf](#creating-an-autoruninf-file). Este archivo especifica una aplicación de instalación que se ejecutará, junto con una variedad de configuraciones opcionales. La aplicación de inicio normalmente instala, desinstala, configura y, quizás, ejecuta la aplicación.

-   [Creación de un archivo Autorun.inf](#creating-an-autoruninf-file)
-   [La \[ sección \] DeviceInstall](#the-deviceinstall-section)
-   [Temas relacionados](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Creación de un archivo Autorun.inf

Autorun.inf es un archivo de texto ubicado en el directorio raíz del CD-ROM que contiene la aplicación. Su función principal es proporcionar al sistema el nombre y la ubicación del programa de inicio de la aplicación que se ejecutará cuando se inserte el disco.

> [!Note]  
> Los archivos Autorun.inf no se admiten en Windows XP para las unidades que devuelven DRIVE \_ REMOVABLE desde [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

El archivo Autorun.inf también puede contener información opcional, como:

-   Nombre de un archivo que contiene un icono que representará la unidad de CD-ROM de la aplicación. Este icono se mostrará en Windows Explorer en lugar del icono de unidad estándar.
-   Comandos adicionales para el menú contextual que se muestra cuando el usuario hace clic con el botón derecho en el icono de CD-ROM. También puede especificar el comando predeterminado que se ejecuta cuando el usuario hace doble clic en el icono.

Los archivos Autorun.inf son similares a .ini archivos. Constan de una o varias secciones, cada una con un nombre entre corchetes. Cada sección contiene una serie de comandos que ejecutará el Shell cuando se inserte el disco. Hay dos secciones que están definidas actualmente para los archivos Autorun.inf.

-   La **\[ sección \] de ejecución** automática contiene los comandos de ejecución automática predeterminados. Todos los archivos Autorun.inf deben tener una **\[ sección de ejecución \]** automática.
-   Se puede **\[ incluir \] una sección autorun.alpha** opcional para los sistemas que se ejecutan en equipos basados en RISC. Cuando se inserta un disco en una unidad de CD-ROM en un sistema basado en RISC, shell ejecutará los comandos de esta sección en lugar de los de la sección **\[ de ejecución \]** automática.

> [!Note]  
> El shell comprueba primero si hay una sección específica de la arquitectura. Si no encuentra una, usa la información de la **\[ sección de ejecución \]** automática. Una vez que el Shell encuentra una sección, omite todas las demás, por lo que cada sección debe ser independiente.

 

Cada sección contiene una serie de comandos que determinan cómo se realiza la operación de ejecución automática. Hay cinco comandos disponibles.



| Get-Help                         | Descripción                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [defaulticon](autorun-cmds.md) | Especifica el icono predeterminado de la aplicación.                                        |
| [icono](autorun-cmds.md)        | Especifica la ruta de acceso y el nombre de archivo de un icono específico de la aplicación para la unidad de CD-ROM. |
| [open](autorun-cmds.md)        | Especifica la ruta de acceso y el nombre de archivo de la aplicación de inicio.                           |
| [useautorun](autorun-cmds.md)  | Especifica que se deben usar características de Reproducción automática V2 si se admiten.                       |
| [Cáscara](autorun-cmds.md)       | Define el comando predeterminado en el menú contextual del CD-ROM.                             |
| [verbo \_ shell](autorun-cmds.md) | Agrega comandos al menú contextual del CD-ROM.                                           |



 

A continuación se muestra un ejemplo de un archivo Autorun.inf simple. Especifica Filename.exe como aplicación de inicio. El segundo icono de Filename.exe representará la unidad de CD-ROM en lugar del icono de unidad estándar.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Este ejemplo de Autorun.inf ejecuta diferentes aplicaciones de inicio en función del tipo de equipo.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>Sección \[ DeviceInstall \]

Puede usar la sección **\[ DeviceInstall en \]** cualquier medio extraíble. Solo se admite en Windows XP. Use **DriverPath para especificar una ruta** de acceso de directorio en la que Windows XP busque archivos de controlador, lo que evita una búsqueda larga a través de todo el contenido.

Use la sección **\[ DeviceInstall con \]** una instalación de controladores para especificar directorios donde Windows XP debe buscar archivos de controlador en los medios. En Windows XP, ya no se buscan medios completos de forma predeterminada, por lo que se requiere **\[ DeviceInstall \]** para especificar ubicaciones de búsqueda. Estos son los únicos medios extraíbles que Windows XP busca completamente sin una **\[ sección DeviceInstall \]** en un archivo Autorun.inf.

-   Disquetes encontrados en las unidades A o B.
-   Medios de CD/DVD de menos de 1 gigabyte (GB) de tamaño.

Todos los demás medios deben incluir una **\[ sección DeviceInstall \]** para Windows XP para detectar los controladores almacenados en ese medio.

> [!Note]  
> Al igual que **\[ con la sección \] AutoRun** , la sección **\[ DeviceInstall \]** puede ser específica de la arquitectura.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar aplicaciones de inicio de ejecución automática](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Escritura de una aplicación de instalación de dispositivos](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
