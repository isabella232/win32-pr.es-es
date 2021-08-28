---
description: Al desarrollar su propia aplicación VSS, debe observar las siguientes directrices y restricciones.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilidad de aplicaciones de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca1f6f3013856087e70247aed21d8f35aa4cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483021"
---
# <a name="vss-application-compatibility"></a>Compatibilidad de aplicaciones de VSS

Al desarrollar su propia aplicación VSS, debe observar las siguientes directrices y restricciones. Puede resultar útil hacer referencia al código de ejemplo para solicitantes, proveedores y escritores de VSS que se proporciona en el Kit de desarrollo de software (SDK) de Microsoft Windows.

> [!Note]  
> El SDK Windows se puede usar para desarrollar aplicaciones VSS solo para Windows Vista y versiones Windows versiones posteriores del sistema operativo. No se puede usar para desarrollar solicitantes, proveedores o escritores de VSS para Windows Server 2003 R2, Windows Server 2003 o Windows XP.

 

**Windows Server 2003 R2, Windows Server 2003 y Windows XP:** VSS está disponible en el SDK Servicio de instantáneas de volumen 7.2, que puede descargar de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Tenga en cuenta que los archivos vssapi.lib de 64 bits en los directorios del directorio Obj de Win2003 se pueden usar para las versiones de 64 bits de \\ Windows Server 2003 R2, Windows Server 2003 y Windows XP. Este SDK también proporciona código de ejemplo para solicitantes, proveedores y escritores de VSS.

## <a name="compiling-vss-applications"></a>Compilación de aplicaciones vss

Al desarrollar un solicitante, como una aplicación de copia de seguridad:

-   Incluya los encabezados siguientes: <dl> Vss.h  
    VsWriter.h  
    VsBackup.h  
    </dl>
-   Link the following library: <dl> VssApi.Lib  
    </dl>

Al desarrollar un escritor:

-   Incluya los encabezados siguientes: <dl> Vss.h  
    VsWriter.h  
    </dl>
-   Link the following library: <dl> VssApi.lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configuraciones y restricciones admitidas

En la lista siguiente se describen las configuraciones y restricciones admitidas:

-   VSS se proporciona y admite en versiones del sistema operativo Windows a partir de Windows XP.
-   En la tabla siguiente se resume la información de compatibilidad entre Windows versiones anteriores. Tenga en cuenta que si una aplicación VSS está "compilada para" una versión de Windows especificada, esto significa que la aplicación se compiló con los archivos de encabezado y las bibliotecas que son específicas de esa versión.

    > [!Note]  
    > Los proveedores de hardware solo se ejecutarán en Windows versiones del sistema operativo del servidor. No se ejecutarán en Windows del sistema operativo cliente.

     

    > [!Note]  
    > En las tablas siguientes, Windows Server 2008 con Service Pack 2 (SP2) debe considerarse igual que Windows Server 2008. Para obtener más información sobre Windows Server 2008 con SP2, vea <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 debe considerarse igual que Windows Server 2003.

     

    > [!Note]  
    > Si una aplicación VSS se compila para Windows Server 2003 o posterior, también se ejecutará en versiones posteriores de Windows.

     

    

    
| Solicitantes, escritores y proveedores de VSS compilados para | Se ejecutará en | 
|-----------------------------------------------------|-------------|
| Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits) | Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) y Windows Vista (64 bits) | 
| Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits) | Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) y Windows Vista (32 bits) | 
| Windows Server 2003 (64 bits) | Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) y Windows Server 2003 (64 bits) | 
| Windows Server 2003 (32 bits) | Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) y Windows Server 2003 (32 bits)    <blockquote>    [!Note]<br />    Los solicitantes también se ejecutarán Windows Server 2003 (64 bits).    </blockquote><br /> | 
| Windows XP edición de 64 bits | Windows Server 2003 (64 bits) y Windows XP de 64 bits | 
| Windows XP (32 bits) | Windows XP (32 bits) | 


    

     

    

    | Para compilar un solicitante, escritor o proveedor de VSS para        | Uso                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 o Windows 7                        | Windows SDK para Windows 7 (disponible en el [Centro de Windows descarga).](https://www.microsoft.com/download/details.aspx?id=8279)                |
    | Windows Server 2008 o Windows Vista                       | Windows SDK para Windows Server 2008 (disponible en el Centro [para desarrolladores Windows SDK).](https://msdn.microsoft.com/windows/bb980924.aspx) |
    | Windows Server 2003 R2, Windows Server 2003 o Windows XP | [SERVICIO DE INSTANTÁNEAS DE VOLUMEN SDK 7.2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Todas las aplicaciones VSS de 32 bits (solicitantes, proveedores y escritores) deben ejecutarse como aplicaciones nativas de 32 o 64 bits. No se admite su ejecución en WOW64.

    **Windows Server 2003 y Windows XP:** Se admite la ejecución de solicitantes VSS de 32 bits en WOW64, pero no para copias de seguridad de estado del sistema. No se admite la ejecución de escritores y proveedores de VSS de 32 bits en WOW64. Se quitó la compatibilidad con la ejecución de solicitantes de 32 bits en WOW64 en Windows Vista y versiones posteriores.

-   Una instantánea creada en Windows Server 2003 R2 o Windows Server 2003 no se puede usar en un equipo que ejecute Windows Server 2008 R2 o Windows Server 2008. No se puede usar una instantánea creada en Windows Server 2008 R2 o Windows Server 2008 en un equipo que ejecute Windows Server 2003. Sin embargo, se puede usar una instantánea que se creó en Windows Server 2008 en un equipo que ejecuta Windows Server 2008 R2 y viceversa.
-   Para admitir instantáneas, un sistema que ejecute VSS debe tener al menos un sistema de archivos NTFS. Este sistema de archivos hospedará el "área de diferencias" de la instantánea. Para obtener más información, vea [Proveedor del sistema](providers.md).
-   Dada la presencia de un sistema de archivos NTFS y dada la elección adecuada del contexto (consulte Configuraciones de contexto [de instantáneas),](shadow-copy-context-configurations.md)cualquier sistema de archivos local compatible se puede realizar una instantánea.
-   Solo puede realizar instantáneas para sistemas de archivos montados localmente. El sistema que los monta no puede realizar la instantánea de los recursos compartidos remotos y otros sistemas de archivos montados de forma cruzada. Estos sistemas de archivos solo se pueden copiar de forma instantánea en los sistemas que sirven a los sistemas de archivos.
-   Los escritores y solicitantes deben especificar solo los recursos locales. Los recursos locales son conjuntos de archivos cuya ruta de acceso absoluta comienza con una letra de unidad y la letra de unidad no se puede asociar a una carpeta montada en un recurso compartido remoto.
-   El número máximo es de instantáneas de software para cada volumen es 512. Sin embargo, de forma predeterminada solo se pueden mantener 64 instantáneas utilizadas por la característica Instantáneas de carpetas compartidas. Para cambiar el límite de la característica Instantáneas de carpetas compartidas, use la clave del Registro [MaxShadowCopies.](../backup/registry-keys-for-backup-and-restore.md)
-   La infraestructura de componentes de copia de seguridad no admite la copia de seguridad de recursos de clúster como componentes de escritura. Para hacer una copia de seguridad de los recursos del clúster, las aplicaciones deben suponer que la ruta de acceso es local a un nodo de clúster determinado especificado.
-   [!Note]  
    > Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea Windows (todas las versiones).

     

    Al realizar una copia de seguridad y recuperar el estado del sistema, la estrategia recomendada es realizar una copia de seguridad y recuperar los volúmenes del sistema y de arranque, además de los archivos enumerados por los escritores de estado del sistema.

    > [!Note]  
    > Los escritores de estado del sistema son escritores que tienen el atributo [**VSS \_ USAGE \_ TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) establecido en VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

     

 

 
