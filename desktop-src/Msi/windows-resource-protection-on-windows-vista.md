---
description: Windows El instalador se adhiere a Windows Resource Protection (WRP) al instalar archivos esenciales del sistema, carpetas e información del Registro en Windows Server 2008 y versiones posteriores y Windows Vista y versiones posteriores.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Uso Windows Installer y Windows Resource Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063018"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Uso Windows Installer y Windows Resource Protection

Windows El instalador se adhiere a Windows Resource Protection (WRP) al instalar archivos esenciales del sistema, carpetas e información del Registro en Windows Server 2008 y versiones posteriores y Windows Vista y versiones posteriores.

WRP en Windows Server 2008 y Windows Vista reemplaza Windows File Protection (WFP) en Windows Server 2003, Windows XP y Windows 2000. Windows Los desarrolladores del instalador deben tener en cuenta los siguientes cambios en la forma en que el instalador controla los recursos protegidos en Windows Server 2008 y versiones posteriores y Windows Vista y versiones posteriores:

-   Cuando se ejecuta en Windows Server 2008 y versiones posteriores o Windows Vista y versiones posteriores, el instalador de Windows omite la instalación de cualquier archivo protegido por WRP, el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin ningún error. En Windows Server 2003, Windows XP y Windows 2000, cuando el instalador de Windows encontró un archivo protegido por WFP, el instalador solicitaría que WFP instalara el archivo.
-   WRP en Windows Server 2008 y versiones posteriores o Windows Vista y versiones posteriores pueden proteger las claves del Registro además de los archivos. Si el instalador de Windows encuentra una clave del Registro protegida por WRP, el instalador omite la instalación de esa clave del Registro, el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin ningún error.
-   Tenga en cuenta que si un Windows Installer contiene un archivo o una clave del Registro que está protegido por WRP, este recurso debe usarse como KeyPath para el componente. En este caso, Windows instalador no instala, actualiza ni quita el componente. No debe incluir ningún recurso protegido en un paquete de instalación. En su lugar, debe usar los mecanismos de reemplazo de recursos [admitidos](../wfp/supported-file-replacement-mechanisms.md) [para Windows Resource Protection](../wfp/windows-resource-protection-portal.md).

Para obtener más información sobre WRP, [vea Windows Resource Protection](../wfp/windows-resource-protection-portal.md) y la información que se proporciona en Microsoft [Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP para Windows Server 2003 y Windows XP/2000

Windows El instalador se adhiere a Windows File Protection (WFP) al instalar archivos esenciales del sistema en Windows Server 2003, Windows XP y Windows 2000. Si una instalación desatendida de una aplicación modifica un archivo del sistema protegido, WFP restaura el archivo a la versión de archivo comprobada.

Windows El instalador nunca intenta instalar o reemplazar un archivo protegido. Cuando la acción [InstallFiles](installfiles-action.md) o cualquier otra acción programada antes de InstallFiles intenta instalar un archivo protegido en Windows Server 2003, Windows XP o Windows 2000, el instalador llama a WFP con una solicitud para instalar o reemplazar el archivo protegido. El instalador solicita la instalación de archivos de WFP inmediatamente después de ejecutar la acción InstallFiles. WFP instala o reemplaza el archivo en el sistema del usuario por una versión almacenada en caché del archivo protegido. Tenga en cuenta que esto no garantiza que la versión del archivo instalada desde la memoria caché sea la versión requerida por la aplicación. Una vez que WFP ha instalado el archivo, el instalador determina si esta versión coincide con la versión del paquete. Si la versión del archivo del paquete es mayor que la versión instalada, el instalador informa al usuario de que no puede actualizar el sistema y que puede ser necesaria una actualización del sistema operativo para la aplicación.

Si alguna acción secuenciada después de [que InstallFiles](installfiles-action.md) intente instalar o reemplazar un archivo protegido que aún no está instalado en el sistema, el instalador no puede llamar a WFP para instalar el archivo. En este caso, el instalador informa al usuario de que no puede actualizar el sistema y de que puede ser necesaria una actualización del sistema operativo para la aplicación.

El instalador también comprueba con WFP al quitar archivos y nunca intenta quitar archivos del sistema protegidos.

## <a name="component-key-files-protected-by-wfp"></a>Archivos de clave de componente protegidos por WFP

Tenga en cuenta que si un Windows Installer contiene un archivo WFP, este archivo debe especificarse como ruta de acceso de clave para el componente.

Cuando el instalador intenta instalar el archivo de clave de un componente en Windows Server 2003, Windows XP o Windows 2000, primero llama a WFP para determinar si el archivo de clave está protegido. Cuando el archivo de clave de un componente está protegido por WFP y ese archivo de clave ya está instalado, el instalador actualiza el componente solo si la versión del archivo de clave del paquete es mayor que la versión instalada. Si el paquete de instalación especifica que se va a instalar un componente y el archivo de clave del componente no está instalado actualmente, independientemente de si el archivo de clave está protegido, el instalador instala el componente. Una vez instalado cualquier componente que tenga un archivo de clave protegido por WFP, se instala permanentemente y el instalador nunca quita ni reemplaza el componente.

## <a name="installation-of-assemblies-by-wfp"></a>Instalación de ensamblados por WFP

WFP para ensamblados difiere de WFP para archivos del sistema.

WFP protege Windows Server 2003, Windows XP y Windows 2000 mediante la detección de intentos de reemplazar archivos del sistema protegidos. Esta protección se desencadena después de que WFP reciba una notificación de cambio de directorio para un archivo de un directorio protegido. Cuando WFP recibe esta notificación, determina qué archivo ha cambiado. Si el archivo está protegido, WFP busca la firma de archivo en un archivo de catálogo estático para determinar si el nuevo archivo es la versión correcta. Si la versión del archivo no es correcta, el sistema reemplaza el archivo por la versión correcta de los medios de caché o distribución.

Por el contrario, el WFP de ensamblados es dinámico. WFP se extiende a los archivos a medida que se agregan a la caché de ensamblados en paralelo compartida. Si un ensamblado se daña, WFP solicitará al instalador que reemplace el archivo. Windows El instalador puede o no poder reemplazar el archivo en función de si el paquete de origen es accesible. Si no se puede acceder al paquete de origen, WFP mostrará un cuadro de diálogo que indica que no puede restaurar el archivo.

Tenga en cuenta que los ensamblados compartidos no administrados en paralelo, instalados en %windir% winsxs, están protegidos \\ por WFP. Los ensamblados privados no administrados, instalados en el directorio de la aplicación, no están protegidos por WFP. Los ensamblados globales administrados instalados en el directorio de la aplicación o %windir% \\ assembly gac no están protegidos por \\ WFP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Protección de recursos](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
