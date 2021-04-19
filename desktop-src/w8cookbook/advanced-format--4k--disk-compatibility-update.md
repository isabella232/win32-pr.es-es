---
title: Actualización de compatibilidad de disco Advanced Format (4K)
description: Actualización de compatibilidad de disco Advanced Format (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbad505575c4479bd750f09ccd83bc4da4c39667
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314978"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Actualización de compatibilidad de disco Advanced Format (4K)

## <a name="platforms"></a>Plataformas

**Clientes**   de   Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8  
**Servidores**   de   Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 R2 y Windows Server 2016  


## <a name="description"></a>Descripción

Este artículo es una versión actualizada del artículo titulado actualización de compatibilidad de disco de emulación de 512 bytes (512e) que se lanzó para Windows 7 SP1 y Windows Server 2008 R2 SP1. Esta actualización contiene mucha información nueva, algunas de las cuales solo es aplicable a Windows 8 y Windows Server 2012.

Las densidades áreas aumentan anualmente y, con la reciente llegada de discos de 3 TB, los mecanismos de corrección de errores que se usan para tratar la disminución de la señal a la relación de ruido (SNR) se están convirtiendo en un espacio ineficaz. es decir, se requiere una mayor cantidad de sobrecarga para asegurarse de que se pueda usar el medio. Una de las soluciones del sector de almacenamiento para mejorar este mecanismo de corrección de errores consiste en introducir un formato de medios físicos diferente que incluye un tamaño de sector físico mayor. Este nuevo formato de medio físico se denomina formato avanzado. Por lo tanto, ya no es seguro hacer ninguna suposición con respecto al tamaño de sector de los dispositivos de almacenamiento modernos y los desarrolladores deberán estudiar las suposiciones subyacentes a su código para determinar si hay un impacto.

En este tema se presenta el efecto de los dispositivos de almacenamiento de formato avanzado en el software, se explica lo que las aplicaciones pueden hacer para ayudar a admitir este tipo de medios y se describe la infraestructura que Microsoft presentó con Windows Vista, Windows 7 y Windows 8 para permitir que los desarrolladores admitan estos tipos de dispositivos. Aunque el material presentado en este tema proporciona directrices para mejorar la compatibilidad con los discos con formato avanzado, la información se aplica generalmente a todos los sistemas con discos de formato avanzado que ejecutan Windows Vista, Windows 7 y Windows 8.

**Resumen de las nuevas características relacionadas con el sector grande**

En la lista siguiente se resumen las nuevas características que se ofrecen como parte de Windows 8 y Windows Server 2012 para ayudar a mejorar la experiencia de cliente y de desarrollador con discos de sector grande. Descripción más detallada de cada elemento.

-   Se basa en la compatibilidad de Windows 7 SP1 con los discos 4K con emulación (512e) y proporciona compatibilidad completa con la bandeja de entrada para los discos con un tamaño de sector de 4K sin emulación (4K nativo). Algunos escenarios y aplicaciones compatibles incluyen:
    -   Capacidad para instalar Windows y arrancar desde un disco del sector 4K sin emulación (disco nativo 4K)
    -   VHD y nuevo formato de archivo VHDX
    -   Compatibilidad completa con Hyper-v
    -   Copias de seguridad de Windows
    -   Compatibilidad completa en el sistema de archivos NT (NTFS)
    -   Compatibilidad total con nuevos grupos y espacios de almacenamiento (SSP)
    -   Compatibilidad total con Windows Defender
-   Proporciona una nueva API para consultar el tamaño del sector físico (FileFsSectorSizeInformation):
    -   Disponible para volúmenes de red
    -   Se puede emitir a cualquier identificador de archivo
    -   Disponible para aplicaciones sin privilegios
    -   Modelo de uso más descriptivo
-   Incluye la utilidad de línea de comandos fsutil mejorada para consultar el tamaño del sector lógico y físico del volumen con información de alineación (la versión básica de la utilidad sin información de alineación está disponible para Windows 7 con Microsoft KB 982018 y Windows Server 2008 R2 con Microsoft KB 982018)

**Introducción a los discos con formato avanzado (4K)**

Uno de los problemas de la introducción de este cambio en el formato multimedia es la posibilidad de introducir problemas de compatibilidad con el software y el hardware existentes. Como solución de compatibilidad temporal, el sector de almacenamiento presenta inicialmente discos que emulan un disco de sector de 512 bytes normal, pero facilitan la información disponible sobre el tamaño de sector real a través de los comandos estándar de ATA y SCSI. Como resultado de esta emulación, hay, en esencia, dos tamaños de sector:

**Sector lógico:** Unidad que se usa para el direccionamiento de bloque lógico para los medios. También podemos considerarla como la unidad más pequeña de escritura que el almacenamiento puede aceptar. Esta es la emulación.   
**Sector físico:** Unidad para la que se completan las operaciones de lectura y escritura en el dispositivo en una sola operación. Esta es la unidad de escritura atómica.  
 La mayoría de las API de Windows actuales, como IOCTL \_ Disk \_ Get \_ Drive \_ Geometry devolverán el tamaño del sector lógico, pero el tamaño del sector físico se puede recuperar a través del código de control de propiedad de consulta de almacenamiento de ioctl, con la información pertinente incluida en el campo BytesPerPhysicalSector de la estructura del <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ descriptor de alineación de acceso de almacenamiento</a> . <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property"> \_ \_ \_ </a> Esto se describe con más detalle más adelante en el artículo.

**Tipos iniciales de medios de sectores grandes**

El sector del almacenamiento es rápidamente el trabajo de transición a este nuevo tipo de formato avanzado de almacenamiento para los medios que tienen un tamaño de sector físico de 4 KB. Se publicarán dos tipos de medios en el mercado:

**4 KB nativo:** Este medio no tiene ninguna capa de emulación y expone directamente 4 KB como su tamaño de sector físico y lógico. El problema general con este nuevo tipo de medio es que la mayoría de las aplicaciones y los sistemas operativos no consultan y alinean las operaciones de e/s con el tamaño del sector físico, lo que puede dar lugar a operaciones de e/s inesperadas.  
**emulación de 512 bytes (512e):** Este medio tiene un nivel de emulación como se describe en la sección anterior y expone 512 bytes como su tamaño de sector lógico (similar a un disco normal hoy), pero hace que su información de tamaño de sector físico (4 KB) esté disponible. El problema general con este nuevo tipo de medio es que la mayoría de los sistemas operativos y aplicaciones no entienden la existencia del tamaño del sector físico, lo que puede dar lugar a una serie de problemas, como se explica a continuación.  
**Compatibilidad total con Windows para medios de gran sector**

En esta tabla se documenta la Directiva oficial de soporte técnico de Microsoft para varios medios y sus tamaños de sector presentados. Consulte este [artículo de Knowledge Base](https://support.microsoft.com/kb/2510009) para obtener más información.



| Nombres comunes                                  | Tamaño de sector lógico informado | Tamaño de sector físico indicado | Versión de Windows compatible con                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512-Byte nativo, 512n                         | 512 bytes                    | 512 bytes                     | Todas las versiones de Windows                                                                                                                                                                                                                                                                                     |
| Formato avanzado, 512e, AF, emulación de 512 bytes | 512 bytes                    | 4 KB                          | Windows Vista con MS KB 2553708 <br/> Windows Server 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Server 2008 R2 * w/MS KB 982018 <br/> Todas las versiones de Windows de Windows 7 SP1 y posteriores. <br/> Todas las versiones de servidor de Server 2008 R2 SP1 y versiones posteriores. <br/> <br/> \*Excepto para Hyper-V. Vea la sección ["requisitos de compatibilidad de aplicaciones para unidades de sector grande"](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) . |
| Formato avanzado, AF, 4K nativo, 4Kn            | 4 KB                         | 4 KB                          | Todas las versiones de Windows de Windows 8 y posteriores <br/> Todas las versiones de servidor de Windows Server 2012 y versiones posteriores <br/>                                                                                                                                                                                                                                                      |
| Otros                                         | No 4 KB o 512 bytes        | No 4 KB o 512 bytes         | No compatible                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Aunque no se sobrerayó en la tabla anterior, Windows XP, Windows Server 2003 y Windows Server 2003 R2 no admiten medios 512e o 4Kn. Aunque el sistema puede arrancar y ser capaz de funcionar mínimamente, puede haber escenarios desconocidos de problemas de funcionalidad, pérdida de datos o rendimiento poco óptimo. Por lo tanto, Microsoft se recomienda encarecidamente no usar medios de 512e con Windows XP u otros productos basados en el código base de Windows XP (como Windows Home Server 1,0, Windows Server 2003, Windows Server 2003 R2, Windows XP 64-bit Edition, Windows XP Embedded, Windows Small Business Server 2003 y Windows Small Business Server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Cómo funciona la emulación: lectura, modificación y escritura (RMW)

Un medio de almacenamiento tiene una unidad determinada en la que se puede modificar el medio físico. Es decir, los medios solo se pueden escribir o volver a escribir en unidades del tamaño de sector físico. Por lo tanto, las operaciones de escritura que no se realicen en este nivel de unidad necesitarán pasos adicionales, lo que le guiaremos a través del ejemplo siguiente.

En este escenario, una aplicación necesita actualizar el contenido de un registro de Stor ubicado en un sector lógico de 512 bytes. En este diagrama se ilustran los pasos necesarios para que el dispositivo de almacenamiento complete la escritura:

![pasos para que un dispositivo de almacenamiento complete una escritura](images/512ermwsteps.png)

Como se muestra arriba, este proceso implica algún trabajo por parte del dispositivo de almacenamiento que puede provocar una pérdida de rendimiento. Para evitar este trabajo adicional, las aplicaciones deben actualizarse a:

-   Consultar el tamaño del sector físico
-   Asegurarse de que las escrituras se alineen con el tamaño de sector físico indicado

Aunque esto puede parecer solo un problema de rendimiento, puede haber un problema más grave. Vamos a analizar esto en la sección siguiente.

**Resistencia: costo oculto de lectura-modificación-escritura**

La resistencia habla de la capacidad de una aplicación para recuperar el estado entre las sesiones. Hemos detectado lo que es necesario para que un dispositivo de almacenamiento de 512e pueda realizar un sector de 512 bytes para escribir el ciclo de lectura/modificación-escritura. Echemos un vistazo a lo que sucedería si se interrumpiera el proceso de sobrescribir el sector físico anterior en el medio. ¿Cuáles son las consecuencias?

-   Dado que la mayoría de las unidades de disco duro se actualizan de forma local, el sector físico, es decir, la parte del medio en el que se encontró el sector físico podría haberse dañado con información incompleta debido a una sobrescritura parcial. Además, puede pensar en ello como si hubiera perdido los 8 sectores lógicos (que el sector físico contiene lógicamente).
-   Aunque la mayoría de las aplicaciones con un almacén de datos están diseñadas con la capacidad de recuperarse de errores de medios, de la pérdida de ocho sectores o de otro modo, la pérdida de ocho registros de confirmación, puede hacer imposible que el almacén de datos se recupere correctamente. Es posible que un administrador tenga que restaurar manualmente la base de datos a partir de una copia de seguridad o incluso puede tener que realizar una regeneración larga.
-   Un impacto más importante es que el acto de otra aplicación que produce un ciclo de lectura-modificación-escritura puede provocar que se pierdan los datos incluso si la aplicación no se está ejecutando. Esto se debe a que los datos y los demás datos de la aplicación pueden encontrarse en el mismo sector físico.

Teniendo esto en cuenta, es importante que el software de la aplicación vuelva a evaluar las suposiciones tomadas en el código y tenga en cuenta la distinción de tamaño de sector físico lógico, junto con algunos escenarios de cliente interesantes que se describen más adelante en este artículo.

**Hacer lo correcto (evitar Read-Modify-Write)**

Aunque algunos proveedores de almacenamiento pueden estar introduciendo algunos niveles de mitigación en determinados dispositivos de almacenamiento de 512e para intentar facilitar los problemas de rendimiento y resistencia del ciclo de lectura-modificación-escritura, solo hay muchas mitigaciones que pueden controlar en términos de carga de trabajo. Como tal, las aplicaciones no deben basarse en esta mitigación como una solución a largo plazo. Además, no hay ninguna garantía de que todas las clases de discos tengan esta mitigación implementada, ni tampoco se garantiza que la mitigación esté bien diseñada.

La solución a esto no es una mitigación en el disco, sino para diseñar aplicaciones que realicen el conjunto adecuado de cosas para ayudar a admitir este tipo de medios. En esta sección se describen escenarios comunes en los que las aplicaciones pueden tener problemas con discos de sector grande y se sugiere una vía de investigación para probar y resolver cada problema.

**Problema 1: la partición no está alineada con un límite de sector físico**

Cuando el administrador o el usuario crea particiones en el disco, es posible que la primera partición no se haya creado en un límite alineado. Esto puede hacer que todas las escrituras posteriores se desalineen en los límites del sector físico. A partir de Windows Vista SP1 y Windows Server 2008, la primera partición se coloca en los primeros 1024 KB del disco (para los discos de 4 GB o más, de lo contrario, la alineación es de 64 KB) que está alineada con un límite de sector físico de 4 KB. Sin embargo, dada la partición predeterminada en Windows XP, una utilidad de creación de particiones de terceros o un uso incorrecto de las API de Windows, es posible que las particiones creadas no estén alineadas con un límite de sector físico. Los desarrolladores deberán asegurarse de que se usan las API correctas para ayudar a garantizar la alineación. Las API recomendadas para ayudar a garantizar la alineación de la partición se describen a continuación.

Las API IVdsPack:: CreateVolume y IVdsPack2:: CreateVolume2 no usan el parámetro de alineación especificado cuando se crea un nuevo volumen, sino que usan el valor predeterminado de alineación para el sistema operativo (anterior a Windows Vista SP1 usará 63 bytes y, después, Windows Vista SP1 usará los valores predeterminados indicados anteriormente). En su lugar, use las API IVdsCreatePartitionEx:: CreatePartitionEx o IVdsAdvancedDisk:: CreatePartition que usan el parámetro de alineación especificado para las aplicaciones que necesitan crear particiones.

La mejor manera de asegurarse de que la alineación sea correcta es hacerlo bien cuando se crea la partición inicialmente. En caso contrario, la aplicación tendrá que tener en cuenta la alineación al realizar operaciones de escritura o de inicialización, lo que puede ser un proceso muy complejo.

**Problema 2: Escrituras no almacenadas en búfer no alineadas con el tamaño de sector físico**

El problema más sencillo es que las escrituras no almacenadas en búfer no se alinean con el tamaño de sector físico indicado de los medios de almacenamiento. Por otro lado, las escrituras almacenadas en búfer se alinean con el tamaño de página 4 KB, lo que casualmente es el tamaño de sector físico de la primera generación de medios de sector grande. Sin embargo, la mayoría de las aplicaciones con un almacén de datos realizan escrituras no almacenadas en búfer y, por lo tanto, deberán asegurarse de que estas escrituras se realicen en unidades del tamaño de sector físico.

Algunos ejemplos de escenarios en los que la e/s de la aplicación resultante no está alineada:

**Los registros de confirmación se rellenan en los sectores de 512 bytes:** Las aplicaciones con un almacén de datos suelen tener algún tipo de registro de confirmación que mantiene información sobre los cambios en los metadatos o mantiene la estructura del almacén de datos. Con el fin de garantizar que la pérdida de un sector no afecte a varios registros, este registro de confirmación se rellena normalmente en un tamaño de sector. Con un disco con un tamaño de sector físico mayor, la aplicación tendrá que consultar el tamaño de sector físico tal como se muestra en la sección anterior y asegurarse de que cada registro de confirmación se rellene hasta ese tamaño. Con un disco de 4K, esto garantiza que no se produzcan errores de e/s. Con un disco 512e, no solo evita el ciclo de lectura-modificación-escritura, sino que ayuda a garantizar que si se perdió un sector físico, solo se perdería un registro de confirmación.  
**Los archivos de registro se escriben en fragmentos no alineados:** La e/s no almacenada en búfer se usa normalmente al actualizar o anexar a un archivo de registro. Las aplicaciones pueden cambiar a e/s almacenadas en búfer, o almacenar internamente las actualizaciones de registro en unidades del tamaño de sector físico para evitar errores de e/s o desencadenar una lectura/modificación-escritura.  
 Para ayudar a determinar si la aplicación emite e/s no almacenada en búfer, asegúrese de incluir la marca de archivo \_ \_ sin \_ marca de almacenamiento en búfer en el parámetro *dwFlagsAndAttributes* cuando llame a la función CreateFile.

Además, si está alineando actualmente las escrituras en el tamaño del sector, lo más probable es que este tamaño de sector sea solo el tamaño del sector lógico, ya que la mayoría de las API existentes que consultan el tamaño del sector del medio simplemente consultan la unidad de direccionamiento que es, el tamaño del sector lógico. El tamaño de sector de interés es el tamaño del sector físico, que es la unidad real de atomicidad. Algunos ejemplos de API que recuperan el tamaño del sector lógico son:

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   el \_ disco ioctl \_ obtiene la \_ \_ geometría de unidad, el \_ disco ioctl obtener la geometría de \_ \_ unidad \_ \_ ex
-   IVdsDisk:: GetProperties, IVdsDisk3:: GetProperties2

Aquí puede consultar el tamaño del sector físico:

**Método preferido para Windows 8**

Con Windows 8, Microsoft ha incorporado una nueva API que permite a los desarrolladores integrar fácilmente la compatibilidad con 4K dentro de sus aplicaciones. Esta nueva API admite incluso un mayor número de escenarios que el método heredado para Windows Vista y Windows 7 que se describe a continuación. Esta API habilita estos escenarios de llamada:

-   Llamar desde una aplicación sin privilegios
-   Llamar a cualquier identificador de archivo válido
-   Llamar a un identificador de archivo en un volumen remoto a través de SMB2
-   Modelo de programación simplificado

La API está en forma de una nueva clase de información, FileFsSectorSizeInformation, con la información de tamaño de sector de FS del archivo de estructura asociado \_ \_ \_ \_ , que se define de la siguiente manera:


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**Método heredado para Windows 7 y Windows Vista**

Windows Vista y Windows Server 2008 introdujeron las API para consultar el tamaño del sector físico del dispositivo de almacenamiento conectado para los controladores de almacenamiento basados en AHCI. Con Windows 7 y Windows Server 2008 R2, a partir de SP1 (o Microsoft Knowledge Base 982018), esta compatibilidad se extiende a los controladores de almacenamiento basados en Storport. Microsoft ha proporcionado un [ejemplo de código](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) en MSDN que detalla cómo una aplicación puede consultar el tamaño del sector físico del volumen.

Aunque el ejemplo de código anterior le permite obtener el tamaño del sector físico del volumen, debe realizar algunas comprobaciones básicas del tamaño del sector físico indicado antes de usarlo, ya que es posible que algunos controladores no devuelvan datos con el formato correcto:

-   Asegúrese de que el tamaño de sector físico indicado es >= el tamaño de sector lógico indicado; Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño de sector lógico indicado
-   Asegúrese de que el tamaño de sector físico indicado sea una potencia de dos. Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño de sector lógico indicado
-   Si el tamaño del sector físico es un valor de potencia de dos entre 512 y 4 KB, debería considerar la posibilidad de usar un tamaño de sector físico redondeado hacia abajo al tamaño del sector lógico indicado.
-   Si el tamaño del sector físico es un valor de potencia de dos superior a 4 KB, debe evaluar la capacidad de la aplicación para controlar este escenario antes de usar ese valor. de lo contrario, debería considerar el uso de un tamaño de sector físico redondeado a 4 KB.

El uso de este IOCTL para obtener el tamaño del sector físico tiene varias limitaciones. Este:

-   Requiere privilegios elevados. Si la aplicación no se ejecuta con privilegios, puede que tenga que escribir una aplicación de servicio de Windows como se indicó anteriormente.
-   No admite volúmenes SMB; también es posible que tenga que escribir una aplicación de servicio de Windows para admitir la consulta de tamaño de sector físico en estos volúmenes.
-   No se puede emitir a ningún identificador de archivo (IOCTL debe emitirse a un identificador de volumen)

**Problema 3: formatos de archivo que se basan en sectores de 512 bytes**

Algunas aplicaciones con formatos de archivo estándar (como VHD 1,0) pueden tener estos archivos codificados de forma rígida para asumir un tamaño de sector de 512 bytes. Por lo tanto, las actualizaciones y escrituras en este archivo darían como resultado un ciclo de lectura-modificación-escritura en el dispositivo, lo que podría dar lugar a problemas de rendimiento y resistencia para los clientes. Sin embargo, hay maneras de que una aplicación proporcione compatibilidad para trabajar en este tipo de medios, por ejemplo:

-   Use el almacenamiento en búfer para asegurarse de que las escrituras se realicen en unidades del tamaño de sector físico
-   Implementar un interno de lectura/modificación-escritura que puede ayudar a garantizar que las actualizaciones se realicen en unidades del tamaño de sector físico indicado
-   Si es posible, rellenar los registros en un sector físico, de tal forma que el relleno se interprete como espacio vacío
-   Considere la posibilidad de volver a diseñar una versión de la estructura de datos de la aplicación compatible con sectores mayores

**Problema 4: el tamaño del sector físico indicado puede cambiar entre sesiones**

Hay muchos escenarios en los que el tamaño de sector físico indicado del almacenamiento subyacente que hospeda el Stor puede cambiar. Lo más común es cuando se migra el Stor a otro volumen, o incluso a través de la red. Un cambio en el tamaño del sector físico indicado puede ser un evento inesperado para muchas aplicaciones y puede dar lugar a que algunas aplicaciones no se reinicialicen.

Este no es el escenario más sencillo de admitir y se menciona aquí como aviso. Debe tener en cuenta los requisitos de movilidad de sus clientes y ajustar su soporte en consecuencia para ayudar a garantizar que los clientes no se vean afectados negativamente mediante el uso de medios de 4K o de 512e.

**Cómo un usuario puede recuperar el tamaño del sector lógico y físico para un volumen**

En la caja con Windows hay una utilidad para mostrar la información de tamaño de sector para un volumen. Las versiones de Windows con fsutil compatible son:

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 con Microsoft KB 982018
-   Windows 7 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1 con Microsoft KB 982018 (V3)
-   Windows Server 2008 R2 con Microsoft KB 982018 (V3)
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Para obtener la información de tamaño de sector, llame a la utilidad como se indica a continuación desde un símbolo del sistema con privilegios elevados:


```
fsutil fsinfo ntfsinfo <drive letter>
```



Un disco de sector 4K con emulación de 512 bytes tiene el campo bytes por sector establecido en 512 y el campo bytes por sector físico establecido en 4096 de la siguiente manera:

![bytes por sector y por sector físico de un disco de sector de 4k con emulación de 512 bytes](images/4ksectordiskwith512emulation.png)

Un disco nativo 4K tiene los campos bytes por sector y bytes por sector físico establecidos en 4096 de la siguiente manera:

![bytes por sector y por sector físico de un disco nativo de 4k](images/4knativedisk.png)

> [!Note]  
> Si el campo byte por sector físico muestra no compatible, significa que el controlador de almacenamiento no admite la \_ propiedad de consulta de almacenamiento ioctl o que \_ \_ se produjo un error al recuperar la información.

 

## <a name="resources"></a>Recursos

-   [Instrucción de soporte general de Windows](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [Revisión para Windows 7 y Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Revisión para Windows Vista y Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [Declaración de compatibilidad de HyperV](https://support.microsoft.com/kb/2515143)
-   [Información general sobre el \_ código de \_ control de propiedad de consulta de almacenamiento ioctl \_](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [\_Código de \_ control de propiedad de consulta de almacenamiento ioctl \_](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Información general sobre la \_ estructura de \_ descriptor de alineación de acceso de almacenamiento \_](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Descripción de la terminología estándar que se usa para describir las actualizaciones de software de Microsoft](https://support.microsoft.com/kb/824684/)
-   [Código de ejemplo de WDK con detalles sobre cómo extraer la información de alineación de acceso de almacenamiento de la \_ estructura de descriptor de alineación de acceso de almacenamiento \_ \_ al realizar una llamada al \_ código de control de \_ propiedad de consulta de almacenamiento ioctl \_](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Información general sobre las opciones de Command-Line de ImageX](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Requisitos del controlador del chipset Intel para admitir unidades del sector de 4 KB](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

