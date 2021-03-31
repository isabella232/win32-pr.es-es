---
description: Al realizar una copia de seguridad o restauración de VSS, el estado del sistema de Windows se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre se deben tratar como una unidad mediante operaciones de copia de seguridad y restauración.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Copia de seguridad y restauración del estado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812806"
---
# <a name="backing-up-and-restoring-system-state"></a>Copia de seguridad y restauración del estado del sistema

> [!Note]  
> Este tema se aplica a Windows Vista, Windows Server 2008 y versiones posteriores. Para obtener información acerca de Windows Server 2003, consulte [copia de seguridad y restauración del estado del sistema en Windows server 2003 R2 y Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md) .

 

Al realizar una copia de seguridad o restauración de VSS, el estado del sistema de Windows se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre se deben tratar como una unidad mediante operaciones de copia de seguridad y restauración.

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones).

 

Al realizar copias de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar copias de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema. Los escritores de estado del sistema son escritores que tienen el atributo [**\_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Si un escritor de VSS se identifica mediante [**su \_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) como escritor de estado del sistema, debe estar incluido en una copia de seguridad del estado del sistema, incluso si es seleccionable.

 

Además de los archivos binarios del sistema operativo enumerados y controladores enumerados por los escritores de estado del sistema, hay algunos otros archivos de los que se debe hacer una copia de seguridad como parte del estado del sistema.

Todos los componentes indicados por un escritor de estado del sistema de VSS forman parte del estado del sistema, excepto aquellos para los que \_ \_ se establece la marca de estado CF no sistema de VSS \_ \_ .

Los programas de copia de seguridad también deben establecer la clave del registro **LastRestoreId** . Para obtener más información, vea [claves y valores del registro para copias de seguridad y restauración](../backup/registry-keys-for-backup-and-restore.md).

> [!Note]  
> En Windows Vista, Windows Server 2008 y versiones posteriores, se han cambiado los nombres y las ubicaciones de algunos archivos del sistema como se indica a continuación.

 

## <a name="system-state"></a>Estado del sistema

En Windows Server 2012 y versiones posteriores, además de los archivos que informan los diversos escritores de Estados del sistema VSS, solo es necesario incluir explícitamente los siguientes archivos de licencias, y es necesario excluir explícitamente los siguientes archivos DRM.

## <a name="windows-media-digital-rights-management-files"></a>Archivos Rights Management digitales de Windows Media

En Windows Server 2008 y versiones posteriores, los siguientes archivos, incluidos todos los subdirectorios de la ruta de acceso siguiente, se excluyen del estado del sistema y no deben realizarse copias de seguridad:

-   % ProgramData% \\ DRM de Microsoft \\ Windows \\\\

Esto reemplaza la información de la sección Rights Management digital de Windows Media de [trabajar con el sistema de archivos y las características de seguridad](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>Archivos de configuración del contador de rendimiento

Los archivos de configuración del contador de rendimiento se encuentran en el directorio% SystemRoot% \\ system32 \\ y tienen los siguientes nombres:

<dl> ¿Rendimiento? 00? incrementa  
??. Perfc0 incrementa  
??. Perfd0 incrementa  
??. Perfh0 incrementa  
??. Perfi0 incrementa  
???. Prfc0 incrementa  
???. Prfd0 incrementa  
???. Prfh0 incrementa  
???. Prfi0 incrementa  
</dl>

Estos archivos solo se modifican durante la instalación de la aplicación y se deben realizar copias de seguridad y restaurar durante las copias de seguridad y restauraciones del estado del sistema.

## <a name="iis-configuration-files"></a>Archivos de configuración de IIS

> [!Note]  
> En Windows Vista con Service Pack 1 (SP1) y versiones posteriores, no debe hacer una copia de seguridad de estos archivos. En su lugar, use el escritor de configuración de IIS en la caja. Para obtener más información sobre este escritor, consulte [escritores de VSS en la caja](in-box-vss-writers.md).

 

A continuación se enumeran los archivos de configuración de IIS relevantes y sus ubicaciones:

-   El archivo de machine.config de .NET FX se encuentra en el directorio de la versión de Framework.
-   El archivo web.config raíz ASP.NET se encuentra en el directorio de la versión de .NET Framework.
    > [!Note]  
    > Los archivos de configuración de .NET FX y ASP.NET se encuentran en el directorio de versión de Framework. Si hay varias versiones de Framework instaladas en el equipo, este directorio contendrá un archivo de configuración para cada versión instalada.

     

-   El archivo de configuración central de IIS applicationHost.config se encuentra en el directorio% WINDIR% \\ system32 \\ Inetsrv \\ config. Para que el servidor comprenda este archivo de configuración, hay archivos de esquema que determinan su gramática y estructura. Estos archivos se encuentran en el directorio% WINDIR% \\ system32 \\ Inetsrv \\ config \\ Schema.

La ruta de acceso del directorio de la versión de Framework se almacena en la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ . NETFramework \\ InstallRoot**

Además, se debe realizar una copia de seguridad de las claves de cifrado siguientes:<dl> % ProgramData% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*  
% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Archivos de marco

Se debe realizar una copia de seguridad de todas las versiones de .NET Framework. Los archivos se encuentran en uno de los siguientes directorios o en ambos:

<dl> % WINDIR% \\ Microsoft.net \\ Framework  
% WINDIR% \\ Microsoft.net \\ Framework64  
</dl>

Además, se debe realizar una copia de seguridad de los archivos de ensamblado. Estos archivos están ubicados en el directorio siguiente:<dl> % WINDIR% \\ Assembly  
</dl>

## <a name="task-scheduler-task-files"></a>Archivos de tareas de Programador de tareas

Se debe realizar una copia de seguridad de los archivos de tarea del programador de tareas. Los archivos se encuentran en una o las dos ubicaciones siguientes:

<dl> % WINDIR% \\ system32 \\ Tasks y cualquier subdirectorio (recursivamente)  
% WINDIR% \\ Tasks (sin subdirectorios)  
</dl>

 

 
