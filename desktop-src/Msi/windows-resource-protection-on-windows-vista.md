---
description: Windows Installer se adhiere a Protección de recursos de Windows (WRP) al instalar archivos esenciales del sistema, carpetas e información del registro en Windows Server 2008 y versiones posteriores, y en Windows Vista y versiones posteriores.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Usar Windows Installer y Protección de recursos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002192"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Usar Windows Installer y Protección de recursos de Windows

Windows Installer se adhiere a Protección de recursos de Windows (WRP) al instalar archivos esenciales del sistema, carpetas e información del registro en Windows Server 2008 y versiones posteriores, y en Windows Vista y versiones posteriores.

WRP en Windows Server 2008 y Windows Vista reemplaza a la protección de archivos de Windows (WFP) en Windows Server 2003, Windows XP y Windows 2000. Windows Installer los desarrolladores deben tener en cuenta los siguientes cambios en la forma en que el instalador controla los recursos protegidos en Windows Server 2008 y versiones posteriores, y en Windows Vista y versiones posteriores:

-   Cuando se ejecuta en Windows Server 2008 y versiones posteriores o Windows Vista y versiones posteriores, el Windows Installer omite la instalación de cualquier archivo que esté protegido por WRP, el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin un error. En Windows Server 2003, Windows XP y Windows 2000, cuando el Windows Installer encontró un archivo protegido con WFP, el instalador solicitaría que WFP instalara el archivo.
-   WRP en Windows Server 2008 y versiones posteriores o Windows Vista y versiones posteriores pueden proteger las claves del registro además de los archivos. Si el Windows Installer encuentra una clave del registro protegida por WRP, el instalador omite la instalación de esa clave del registro, el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin un error.
-   Tenga en cuenta que si un componente de Windows Installer contiene un archivo o una clave del registro que está protegida por WRP, este recurso debe usarse como la ruta de acceso del componente. En este caso, Windows Installer no instala, actualiza o quita el componente. No debe incluir ningún recurso protegido en un paquete de instalación. En su lugar, debe usar los [mecanismos de sustitución de recursos admitidos](../wfp/supported-file-replacement-mechanisms.md) para [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md).

Para obtener más información acerca de WRP, consulte [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) e información que se proporciona en [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP para Windows Server 2003 y Windows XP/2000

Windows Installer se adhiere a la protección de archivos de Windows (WFP) al instalar archivos esenciales del sistema en Windows Server 2003, Windows XP y Windows 2000. Si un archivo del sistema protegido es modificado por una instalación desatendida de una aplicación, WFP restaura el archivo a la versión comprobada del archivo.

Windows Installer nunca intenta instalar o reemplazar un archivo protegido. Cuando la acción [InstallFiles](installfiles-action.md) o cualquier otra acción programada antes de la InstallFiles intenta instalar un archivo protegido en windows Server 2003, Windows XP o Windows 2000, el instalador llama a WFP con una solicitud para instalar o reemplazar el archivo protegido. El instalador solicita la instalación de archivos desde WFP inmediatamente después de ejecutar la acción InstallFiles. WFP instala o reemplaza el archivo en el sistema del usuario con una versión almacenada en caché del archivo protegido. Tenga en cuenta que esto no garantiza que la versión del archivo instalada desde la memoria caché sea la versión requerida por la aplicación. Después de que WFP haya instalado el archivo, el instalador determina si esta versión coincide con la versión del paquete. Si la versión del archivo en el paquete es mayor que la versión instalada, el instalador informa al usuario de que no puede actualizar el sistema y que es posible que se requiera una actualización del sistema operativo para la aplicación.

Si alguna acción secuenciada después de la [InstallFiles](installfiles-action.md) intenta instalar o reemplazar un archivo protegido que no está instalado en el sistema, el instalador no podrá llamar a WFP para instalar el archivo. En este caso, el instalador informa al usuario de que no puede actualizar el sistema y que es posible que se requiera una actualización del sistema operativo para la aplicación.

El instalador también comprueba con WFP cuando quita archivos y nunca intenta quitar archivos del sistema protegidos.

## <a name="component-key-files-protected-by-wfp"></a>Archivos de clave de componente protegidos por WFP

Tenga en cuenta que si un componente de Windows Installer contiene un archivo WFP, este archivo debe especificarse como la ruta de acceso de la clave del componente.

Cuando el instalador intenta instalar el archivo de clave de un componente en Windows Server 2003, Windows XP o Windows 2000, primero llama a WFP para determinar si el archivo de claves está protegido. Cuando el archivo de clave de un componente está protegido por WFP y ese archivo de clave ya está instalado, el instalador actualiza el componente solo si la versión del archivo de clave del paquete es mayor que la versión instalada. Si el paquete de instalación especifica que se debe instalar un componente y el archivo de clave del componente no está instalado actualmente, independientemente de si el archivo de clave está protegido, el instalador instala el componente. Una vez instalado cualquier componente que tenga un archivo de clave protegido por WFP, se instalará de forma permanente y el instalador nunca quitará o reemplazará al componente.

## <a name="installation-of-assemblies-by-wfp"></a>Instalación de ensamblados por WFP

WFP para ensamblados difiere de WFP para archivos del sistema.

WFP protege los archivos del sistema de Windows Server 2003, Windows XP y Windows 2000 al detectar intentos de reemplazar archivos del sistema protegidos. Esta protección se desencadena después de que WFP reciba una notificación de cambio de directorio para un archivo en un directorio protegido. Cuando WFP recibe esta notificación, determina qué archivo ha cambiado. Si el archivo está protegido, WFP busca la firma de archivo en un archivo de catálogo estático para determinar si el nuevo archivo es la versión correcta. Si la versión del archivo no es correcta, el sistema reemplaza el archivo con la versión correcta de la caché o del medio de distribución.

Por el contrario, WFP de ensamblados es dinámico. WFP se extiende a los archivos a medida que se agregan a la caché de ensamblados en paralelo compartida. Si un ensamblado se daña, WFP solicitará que el instalador Reemplace el archivo. Windows Installer puede o no reemplazar el archivo en función de si el paquete de origen es accesible. Si no se puede tener acceso al paquete de origen, WFP abrirá un cuadro de diálogo que indica que no se puede restaurar el archivo.

Tenga en cuenta que los ensamblados en paralelo no administrados, instalados en% WINDIR% \\ WinSxS, están protegidos por WFP. Los ensamblados privados no administrados, instalados en el directorio de la aplicación, no están protegidos por WFP. Los ensamblados globales administrados instalados en el directorio de la aplicación o en la GAC del ensamblado% WINDIR% \\ \\ no están protegidos por WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de recursos de Windows](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
