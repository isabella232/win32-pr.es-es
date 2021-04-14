---
description: Al desarrollar su propia aplicación de VSS, debe respetar las siguientes directrices y restricciones.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilidad de aplicaciones de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360315"
---
# <a name="vss-application-compatibility"></a>Compatibilidad de aplicaciones de VSS

Al desarrollar su propia aplicación de VSS, debe respetar las siguientes directrices y restricciones. Puede que le resulte útil consultar el código de ejemplo de los solicitantes, proveedores y escritores de VSS que se proporcionan en el kit de desarrollo de software (SDK) de Microsoft Windows.

> [!Note]  
> El Windows SDK se puede usar para desarrollar aplicaciones VSS solo para Windows Vista y versiones posteriores del sistema operativo Windows. No se puede usar para desarrollar solicitantes, proveedores o escritores de VSS para Windows Server 2003 R2, Windows Server 2003 o Windows XP.

 

**Windows server 2003 R2, Windows server 2003 y Windows XP:** VSS está disponible en el SDK de Servicio de instantáneas de volumen 7,2, que puede descargar de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Tenga en cuenta que los archivos vssapi. lib de 64 bits en los directorios del \\ directorio obj de Win2003 se pueden usar para las versiones de 64 bits de Windows server 2003 R2, Windows server 2003 y Windows XP. Este SDK también proporciona código de ejemplo para los solicitantes, proveedores y escritores de VSS.

## <a name="compiling-vss-applications"></a>Compilar aplicaciones VSS

Al desarrollar un solicitante, como una aplicación de copia de seguridad:

-   Incluya los encabezados siguientes: <dl> VSS. h  
    VsWriter. h  
    VsBackup. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

Al desarrollar un escritor:

-   Incluya los encabezados siguientes: <dl> VSS. h  
    VsWriter. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configuraciones y restricciones admitidas

En la lista siguiente se describen las configuraciones admitidas y las restricciones:

-   Se proporciona VSS y se admite en las versiones del sistema operativo Windows a partir de Windows XP.
-   En la tabla siguiente se resume la información de compatibilidad entre las versiones de Windows. Tenga en cuenta que si una aplicación VSS se "compila para" una versión de Windows especificada, significa que la aplicación se compiló con los archivos de encabezado y las bibliotecas que son específicas de esa versión.

    > [!Note]  
    > Los proveedores de hardware solo se ejecutarán en las versiones del sistema operativo Windows Server. No se ejecutarán en las versiones de sistema operativo de cliente de Windows.

     

    > [!Note]  
    > En las tablas siguientes, Windows Server 2008 con Service Pack 2 (SP2) debe considerarse igual que Windows Server 2008. Para obtener más información acerca de Windows Server 2008 con SP2, vea <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 debe considerarse igual que Windows Server 2003.

     

    > [!Note]  
    > Si se compila una aplicación de VSS para Windows Server 2003 o una versión posterior, también se ejecutará en versiones posteriores de Windows.

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Solicitantes, escritores y proveedores de VSS compilados para</th>
    <th>Se ejecutará el</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits)</td>
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits)</td>
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits)</td>
    </tr>
    <tr class="odd">
    <td>Windows Server 2003 (64 bits)</td>
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) y Windows Server 2003 (64 bits)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2003 (32 bits)</td>
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) y Windows Server 2003 (32 bits) <blockquote>
    [!Note]<br />
Los solicitantes también se ejecutarán en Windows Server 2003 (64 bits).
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>Windows XP 64-bit Edition</td>
    <td>Windows Server 2003 (64 bits) y Windows XP 64-bit Edition</td>
    </tr>
    <tr class="even">
    <td>Windows XP (32 bits)</td>
    <td>Windows XP (32 bits)</td>
    </tr>
    </tbody>
    </table>

    

     

    

    | Para compilar un solicitante, escritor o proveedor de VSS para        | Use                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 o Windows 7                        | Windows SDK para Windows 7 (disponible en el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279)).                |
    | Windows Server 2008 o Windows Vista                       | Windows SDK para Windows Server 2008 (disponible en el [Centro para desarrolladores de Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx)). |
    | Windows Server 2003 R2, Windows Server 2003 o Windows XP | [SDK de Servicio de instantáneas de volumen 7,2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 bits o de 64 bits. No se admite su ejecución en WOW64.

    **Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes de VSS de 32 bits bajo WOW64, pero no para copias de seguridad de estado del sistema. No se admite la ejecución de proveedores y escritores de VSS de 32 bits en WOW64. Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.

-   Una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 no se puede usar en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008. Una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 no se puede usar en un equipo que ejecute Windows Server 2003. Sin embargo, una instantánea creada en Windows Server 2008 puede usarse en un equipo que ejecute Windows Server 2008 R2 y viceversa.
-   Para admitir instantáneas, un sistema que ejecute VSS debe tener al menos un sistema de archivos NTFS. Este sistema de archivos hospedará el "área de diferencias" de la instantánea. Para obtener más información, vea [proveedor del sistema](providers.md).
-   Dada la presencia de un sistema de archivos NTFS y dada la elección de contexto adecuada (vea [configuraciones de contexto de instantáneas](shadow-copy-context-configurations.md)), se puede realizar una instantánea de cualquier sistema de archivos local compatible.
-   Solo puede hacer instantáneas para sistemas de archivos montados localmente. Los recursos compartidos remotos y otros sistemas de archivos entre montajes no pueden ser copiados por el sistema que los monta. Solo pueden realizarse instantáneas de estos sistemas de archivos los sistemas que prestan servicio a los sistemas de archivos.
-   Los escritores y los solicitantes solo deben especificar recursos locales. Los recursos locales son conjuntos de archivos cuya ruta de acceso absoluta empieza con una letra de unidad y la letra de unidad no se puede asociar a una carpeta montada en un recurso compartido remoto.
-   El número máximo de instantáneas de software para cada volumen es 512. Sin embargo, de forma predeterminada solo se pueden mantener 64 instantáneas utilizadas por la característica Instantáneas de carpetas compartidas. Para cambiar el límite de la característica instantáneas de carpetas compartidas, utilice la clave del registro [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .
-   La infraestructura de componentes de copia de seguridad no admite la copia de seguridad de recursos de clúster como componentes del escritor. Para realizar una copia de seguridad de los recursos del clúster, las aplicaciones deben suponer que la ruta de acceso es local a un determinado nodo de clúster.
-   [!Note]  
    > Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones).

     

    Al realizar copias de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar copias de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema.

    > [!Note]  
    > Los escritores de estado del sistema son escritores que tienen el atributo [**\_ \_ tipo de uso de VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

     

 

 
