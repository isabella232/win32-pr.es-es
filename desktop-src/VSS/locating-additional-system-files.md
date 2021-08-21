---
description: Al realizar una copia de seguridad o restauración de VSS, Windows estado del sistema se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre deben tratarse como una unidad mediante operaciones de copia de seguridad y restauración.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Copia de seguridad y restauración del estado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b027fa0d1a01f3d4f735494d34d4f2da2d07a0e0d82ecfd189f7a9c7c8537c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056403"
---
# <a name="backing-up-and-restoring-system-state"></a>Copia de seguridad y restauración del estado del sistema

> [!Note]  
> Este tema se aplica a Windows Vista, Windows Server 2008 y versiones posteriores. Para obtener información sobre Windows Server 2003, vea Copia de seguridad y restauración del estado del sistema en [Windows Server 2003 R2 y Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)

 

Al realizar una copia de seguridad o restauración de VSS, Windows estado del sistema se define como una colección de varios elementos clave del sistema operativo y sus archivos. Estos elementos siempre deben tratarse como una unidad mediante operaciones de copia de seguridad y restauración.

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores ni profesionales de TI para implementar restauraciones de estado del sistema en línea Windows (todas las versiones).

 

Al realizar una copia de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar una copia de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema. Los escritores de estado del sistema son escritores que tienen el atributo [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Si VSS Writer se identifica mediante su [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) como escritor de estado del sistema, debe incluirse en una copia de seguridad de estado del sistema incluso si se puede seleccionar.

 

Además de los archivos binarios enumerados del sistema operativo y del controlador enumerados por los escritores de estado del sistema, hay otros archivos de los que se debe realizar una copia de seguridad como parte del estado del sistema.

Todos los componentes notificados por un sistema de escritura de estado de VSS forman parte del estado del sistema, excepto aquellos para los que se establece la marca VSS \_ CF \_ NOT SYSTEM \_ \_ STATE.

Los programas de copia de seguridad también deben establecer la clave del Registro **LastRestoreId.** Para obtener más información, vea Claves y valores [del Registro para copia de seguridad y restauración.](../backup/registry-keys-for-backup-and-restore.md)

> [!Note]  
> En Windows Vista, Windows Server 2008 y versiones posteriores, los nombres y las ubicaciones de algunos archivos del sistema se han cambiado como se muestra a continuación.

 

## <a name="system-state"></a>Estado del sistema

Para Windows Server 2012 y versiones posteriores, además de los archivos notificados por los distintos escritores de estado del sistema de VSS, solo se deben incluir explícitamente los siguientes archivos de licencia y los siguientes archivos DRM deben excluirse explícitamente.

## <a name="windows-media-digital-rights-management-files"></a>Windows Archivos de archivos Rights Management multimedia digitales

En Windows Server 2008 y versiones posteriores, los siguientes archivos, incluidos todos los subdirectorios de la ruta de acceso siguiente, se excluyen del estado del sistema y no se debe realizar una copia de seguridad:

-   %ProgramData% \\ Microsoft \\ Windows \\ DRM\\

Esto sustituye a la información de la sección Windows Media Digital Rights Management trabajar con características [de seguridad y sistema de archivos](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>Archivos de configuración del contador de rendimiento

Los archivos de configuración del contador de rendimiento se encuentran en el directorio %SystemRoot% \\ System32 \\ y tienen los nombres siguientes:

<dl> ¿Perf?00?. Dat  
Perfc0??. Dat  
Perfd0??. Dat  
Perfh0??. Dat  
Perfi0??. Dat  
Prfc0???. Dat  
Prfd0???. Dat  
Prfh0???. Dat  
Prfi0???. Dat  
</dl>

Estos archivos solo se modifican durante la instalación de la aplicación y deben realizarse copias de seguridad y restaurarse durante las copias de seguridad y restauraciones del estado del sistema.

## <a name="iis-configuration-files"></a>Archivos de configuración de IIS

> [!Note]  
> En Windows Vista con Service Pack 1 (SP1) y versiones posteriores, no debe hacer una copia de seguridad de estos archivos. En su lugar, use el sistema de escritura de configuración de IIS en el cuadro. Para obtener más información sobre este escritor, vea [In-Box VSS Writers](in-box-vss-writers.md).

 

A continuación se enumeran los archivos de configuración de IIS pertinentes y sus ubicaciones:

-   El archivo de machine.config .NET FX se encuentra en el directorio de versión del marco.
-   El ASP.NET de web.config raíz se encuentra en el directorio de versión del marco.
    > [!Note]  
    > Los archivos de configuración de .NET FX y ASP.NET están en el directorio de versión del marco. Si hay varias versiones del marco de trabajo instaladas en el equipo, este directorio contendrá un archivo de configuración para cada versión instalada.

     

-   El archivo applicationHost.config de configuración central de IIS se encuentra en el directorio de configuración \\ \\ inetsrv %windir% \\ system32. Para que el servidor comprenda este archivo de configuración, hay archivos de esquema que determinan su gramática y estructura. Estos archivos se encuentran en el directorio de esquema de configuración %windir% \\ system32 \\ inetsrv. \\ \\

La ruta de acceso del directorio de versión del marco de trabajo se almacena en la siguiente clave del Registro:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ . NETFramework \\ InstallRoot**

Además, se debe realizar una copia de seguridad de las siguientes claves de criptografía:<dl> %ProgramData% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\*  
%SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Archivos de marco

Se debe realizar una copia de seguridad de todas las versiones de .NET Framework. Los archivos se encuentran en uno o ambos directorios siguientes:

<dl> %windir% \\ Microsoft.Net \\ Framework  
%windir% \\ Microsoft.Net \\ Framework64  
</dl>

Además, se debe realizar una copia de seguridad de los archivos de ensamblado. Estos archivos están ubicados en el directorio siguiente:<dl> %windir% \\ assembly  
</dl>

## <a name="task-scheduler-task-files"></a>Programador de tareas de tareas

Se debe realizar una copia de seguridad de los archivos de tareas del programador de tareas. Los archivos se encuentran en una o ambas de las ubicaciones siguientes:

<dl> %windir% \\ system32 \\ tasks and any subdirectories (recursively) (%windir% system32 tasks and any subdirectories (recursively) (%windir% system32 tasks and any subdirectories [%windir% system  
%windir% \\ tareas (sin subdirectorios)  
</dl>

 

 
