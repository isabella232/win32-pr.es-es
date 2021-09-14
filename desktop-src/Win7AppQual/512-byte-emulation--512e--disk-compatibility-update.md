---
description: En este tema se presenta el efecto de los dispositivos de almacenamiento de formato avanzado en el software, se describe qué pueden hacer las aplicaciones para ayudar a admitir este tipo de medios y se describe la infraestructura que Microsoft introdujo con Windows 7 SP1 y Windows Server 2008 R2 SP1 para permitir que los desarrolladores admitan estos tipos de dispositivos.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Actualización de compatibilidad de disco de emulación de 512 bytes (512e)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b654473fa8be5fbea997bd063df2c1f898a7d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249453"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Actualización de compatibilidad de disco de emulación de 512 bytes (512e)

## <a name="platform"></a>Plataforma

 **Clientes:** Windows Vista, Windows 7, Windows 7 SP1  
**Servidores:** Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** alta  
**Frecuencia:** alta  









## <a name="description"></a>Descripción

Las densidades areales aumentan cada año y, con la reciente llegada de discos de 3 TB, los mecanismos de corrección de errores usados para tratar con la reducción de la relación señal-ruido (SNR) se están convirtiendo en espacio ineficaz; es decir, se requiere una mayor cantidad de sobrecarga para garantizar que los medios se pueden usar. Una de las soluciones del sector del almacenamiento para mejorar este mecanismo de corrección de errores es introducir un formato multimedia físico diferente que incluya un tamaño de sector físico mayor. Este nuevo formato de medios físicos se denomina *Formato avanzado.* Por lo tanto, ya no es seguro realizar suposiciones con respecto al tamaño del sector de los dispositivos de almacenamiento modernos, y los desarrolladores tendrán que estudiar las suposiciones subyacentes a su código para determinar si hay un impacto.

En este tema se presenta el efecto de los dispositivos de almacenamiento de formato avanzado en el software, se describe qué pueden hacer las aplicaciones para ayudar a admitir este tipo de medios y se describe la infraestructura para permitir que los desarrolladores admitan estos tipos de dispositivos. Aunque el material presentado en este tema proporciona instrucciones para mejorar la compatibilidad con discos de formato avanzado, la información se aplica generalmente a todos los sistemas con discos de formato avanzado. Las siguientes versiones de Windows proporcionan compatibilidad para consultar el tamaño del sector físico:

-   Windows 7 con Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Para obtener más información, vea Información sobre la directiva de soporte técnico de Microsoft para [unidades](https://support.microsoft.com/kb/2510009)de gran sector en Windows .

Para obtener más información sobre los discos de formato avanzado, póngase en contacto con el proveedor de almacenamiento.

## <a name="logical-vs-physical-sector-size"></a>Tamaño del sector lógico frente al físico

Una de las preocupaciones a la hora de introducir este cambio en el formato multimedia es la compatibilidad con el software y el hardware disponibles actualmente en el mercado. Como solución temporal, el sector de almacenamiento inicialmente introduce discos que emulan un disco de sector normal de 512 bytes, pero que hacen que la información disponible sobre el verdadero tamaño del sector se realice a través de comandos estándar ATA y SCSI. Como resultado de esta emulación, hay dos tamaños de sector:

-   **Sector lógico:** unidad que se usa para el direccionamiento de bloque lógico para los medios. También podemos pensar en ella como la unidad de escritura más pequeña que el almacenamiento puede aceptar. Esta es la emulación.

-   **Sector físico:** unidad para la que las operaciones de lectura y escritura en el dispositivo se completan en una sola operación. Esta es la unidad de escritura atómica.

La mayoría de las API de Windows actuales, como **IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY,** devolverán el tamaño del sector lógico, pero el tamaño del sector físico se puede recuperar a través del código de control [IOCTL STORAGE QUERY \_ \_ \_ PROPERTY,](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) con la información pertinente contenida en el **campo BytesPerPhysicalSector en** la estructura [ \_ \_ \_ DESCRIPTOR](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) DE ALINEACIÓN DE ACCESO DE ALMACENAMIENTO. Esto se describe con más detalle más adelante en el artículo.

## <a name="initial-types-of-large-sector-media"></a>Tipos iniciales de medios de sector grande

El sector del almacenamiento está arrasando rápidamente los esfuerzos para realizar la transición a este nuevo tipo de almacenamiento de formato avanzado para medios con tamaños de sector físico de 4 KB. Se lanzarán al mercado dos tipos de medios:

-   **4 KB nativo:** este medio no tiene ninguna capa de emulación y expone directamente 4 KB como su tamaño de sector lógico y físico. Actualmente, este medio no es compatible con Windows y la mayoría de los demás sistemas operativos. Sin embargo, Microsoft está realizando una investigación sobre la viabilidad de admitir este tipo de medios en una versión futura de Windows y emitirá un artículo de Knowledge Base cuando corresponda.
-   **Emulación de 512 bytes (512e):** este medio tiene una capa de emulación como se explicó en la sección anterior y expone 512 bytes como su tamaño de sector lógico (similar a un disco normal en la actualidad), pero hace que su información de tamaño del sector físico (4 KB) esté disponible. Esto es lo que varios proveedores de almacenamiento presentan actualmente en el mercado. Este problema general con este nuevo tipo de medios es que la mayoría de la aplicación y los sistemas operativos no comprenden la existencia del tamaño del sector físico, lo que puede dar lugar a una serie de problemas, como se analizará a continuación.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funcionamiento de la emulación: lectura y modificación y escritura (RMW)

Un medio de almacenamiento tiene una unidad determinada dentro de la cual se puede modificar el medio físico. Es decir, los medios solo se pueden escribir o reescribir en unidades del tamaño del sector físico. Por lo tanto, las escrituras que no se realizan en este nivel de unidad requerirían pasos adicionales, que se recorrerán en el ejemplo siguiente.

En este escenario, una aplicación debe actualizar el contenido de un registro datastor ubicado dentro de un sector lógico de 512 bytes. En el diagrama siguiente se muestran los pasos necesarios para que el dispositivo de almacenamiento complete la escritura:

![pasos necesarios para actualizar el registro del datastor dentro de un sector lógico de 512 bytes](images/512ermwsteps.png)

Como se ha indicado anteriormente, este proceso implica algún trabajo por parte del dispositivo de almacenamiento que puede provocar una pérdida de rendimiento. Para evitar este trabajo adicional, las aplicaciones deben actualizarse para hacer lo siguiente:

-   Consulta del tamaño del sector físico.
-   Asegúrese de que las escrituras se alinean con el tamaño del sector físico notificado.

## <a name="the-resiliency-impact-of-read-modify-write"></a>El impacto de resistencia de la lectura,modificación y escritura

La resistencia habla de la capacidad de una aplicación para recuperar el estado entre sesiones. Hemos visto lo que es necesario para que un dispositivo de almacenamiento 512e realice una escritura de sector de 512 bytes: el ciclo de lectura y modificación y escritura. Veamos lo que ocurriría si se interrumpa el proceso de sobrescritura del sector físico anterior en los medios. ¿Cuáles serían las consecuencias?

-   Dado que la mayoría de las unidades de disco duro se actualizan en su lugar, el sector físico (es decir, la parte del medio donde se encontraba el sector físico) podría haber estado dañado con información incompleta debido a una sobrescritura parcial. Dicho de otro modo, puede pensar que podría haber perdido los ocho sectores lógicos (que el sector físico contiene lógicamente).

-   Aunque la mayoría de las aplicaciones con un almacén de datos están diseñadas con la capacidad de recuperarse de errores multimedia, la pérdida de ocho sectores o, de otro modo, la pérdida de ocho registros de confirmación, puede hacer que sea imposible que el almacén de datos se recupere correctamente. Es posible que un administrador necesite restaurar manualmente la base de datos a partir de una copia de seguridad o incluso tener que realizar una recompilación larga.

-   Un impacto más importante es que el acto de otra aplicación que provoca un ciclo de lectura,modificación y escritura puede provocar la pérdida de los datos, incluso si la aplicación no se está ejecutando. Esto se debe simplemente a que los datos y los datos de la otra aplicación podrían encontrarse en el mismo sector físico.

Con esto en mente, es importante que el software de la aplicación vuelva a evaluar las suposiciones realizadas en el código y tenga en cuenta la distinción de tamaño del sector lógico-físico, junto con algunos escenarios de clientes interesantes que se debata más adelante en este artículo.

Es más probable que este problema se produzca si la aplicación se basa en un almacén de datos de estructura de registro.

## <a name="avoiding-read-modify-write"></a>Evitar la lectura y modificación y escritura

Aunque algunos proveedores de almacenamiento pueden introducir algunos niveles de mitigación en determinados dispositivos de almacenamiento 512e para intentar facilitar los problemas de rendimiento y resistencia del ciclo de lectura y modificación y escritura, solo hay tanta mitigación que se puede controlar en términos de carga de trabajo. Por lo tanto, las aplicaciones no deben basarse en esta mitigación como una solución a largo plazo.

La solución a esto no es la mitigación en la unidad, sino que las aplicaciones realicen el conjunto correcto de cosas para evitar el ciclo de lectura y modificación y escritura. En esta sección se analizan escenarios comunes en los que las aplicaciones pueden tener problemas con discos de gran sector y se sugiere una vía de investigación para intentar resolver cada problema.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problema 1: La partición no está alineada con un límite de sector físico

Cuando el administrador o el usuario crean particiones en el disco, es posible que la primera partición no se haya creado en un límite alineado. Esto puede hacer que todas las escrituras posteriores no se alineen con los límites del sector físico. A partir de Windows Vista SP1 y Windows Server 2008, la primera partición se coloca en los primeros 1024 KB del disco (para discos de 4 GB o más; de lo contrario, la alineación es de 64 KB) que se alinea con un límite de sector físico de 4 KB. Sin embargo, dada la creación de particiones predeterminada en Windows XP, una utilidad de creación de particiones de terceros o un uso incorrecto de las API de Windows, es posible que las particiones creadas no se alineen con un límite de sector físico. Los desarrolladores tendrán que asegurarse de que se usan las API correctas para ayudar a garantizar la alineación. A continuación se describen las API recomendadas para ayudar a garantizar la alineación de las particiones.

Las API **IVdsPack::CreateVolume** **e IVdsPack2::CreateVolume2** no usan el parámetro de alineación especificado cuando se crea un nuevo volumen y, en su lugar, usan el valor predeterminado de alineación para el sistema operativo (Pre-Windows Vista SP1 usará 63 bytes y, después de Windows Vista SP1, usará los valores predeterminados indicados anteriormente). Por lo tanto, se recomienda que las aplicaciones que necesitan crear particiones usen las API **IVdsCreatePartitionEx::CreatePartitionEx** o **IVdsAdvancedDisk::CreatePartition** en su lugar, que usan el parámetro de alineación especificado.

La mejor manera de ayudar a garantizar que la alineación es correcta es hacerlo correctamente al crear inicialmente la partición. De lo contrario, la aplicación tendrá que tener en cuenta la alineación al realizar escrituras o durante la inicialización, lo que puede ser una cuestión muy compleja. A Windows Vista SP1, esto no suele ser un problema; sin embargo, las versiones anteriores de Windows pueden crear particiones no alineadas que pueden provocar problemas de rendimiento con algunos discos de formato avanzado.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problema 2: Escrituras no almacenadas en búfer no alineadas con el tamaño del sector físico

El problema básico es que las escrituras no almacenadas en búfer no están alineadas con el tamaño del sector físico notificado del medio de almacenamiento, lo que desencadena una lectura,modificación y escritura en la unidad que puede dar lugar a problemas de rendimiento. Por otro lado, las escrituras en búfer se alinean con el tamaño de página (4 KB), que, por coincidencia, es el tamaño del sector físico de la primera generación de medios de sector grande. Sin embargo, la mayoría de las aplicaciones con un almacén de datos realizan escrituras sin almacenamiento en búfer y, por tanto, tendrán que asegurarse de que estas escrituras se realizan en unidades del tamaño del sector físico.

Para ayudar a determinar si la aplicación emite E/S no almacenadas en búfer, compruebe que incluye la marca **FILE \_ FLAG NO \_ \_ BUFFERING** en el parámetro *dwFlagsAndAttributes* al llamar a la función **CreateFile.**

Además, si actualmente está alineando las escrituras con el tamaño del sector, lo más probable es que sea solo el tamaño del *sector* lógico, ya que la mayoría de las API existentes que consultan el tamaño de sector de los medios simplemente consultan la unidad de direccionamiento, es decir, el tamaño del sector lógico. El tamaño del sector de interés aquí es el tamaño del sector físico, que es la unidad real de atomicidad. Algunos ejemplos de API que recuperan el tamaño del sector lógico son:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY**, **IOCTL DISK GET DRIVE \_ GEOMETRY \_ \_ \_ \_ EX**
-   **IVdsDisk::GetProperties**, **IVdsDisk3::GetProperties2**

**Cómo consultar el tamaño del sector físico**

Microsoft ha proporcionado un ejemplo de código en MSDN que detalla cómo una aplicación puede consultar el tamaño del sector físico del volumen. El ejemplo de código se encuentra en <https://msdn.microsoft.com/library/ff800831.aspx> .

Aunque el ejemplo de código anterior le permite obtener el tamaño del sector físico del volumen, debe realizar una comprobación básica del tamaño del sector físico notificado antes de usarlo, ya que se ha observado que algunos controladores pueden no devolver datos con formato correcto:

-   Asegúrese de que el tamaño del sector físico notificado es >= el tamaño del sector lógico notificado. Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño del sector lógico notificado.
-   Asegúrese de que el tamaño del sector físico notificado es una potencia de dos. Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño del sector lógico notificado.
-   Si el tamaño del sector físico es un valor de potencia de dos entre 512 bytes y 4 KB, debe considerar la posibilidad de usar un tamaño de sector físico redondeado al tamaño del sector lógico notificado.
-   Si el tamaño del sector físico es un valor de potencia de dos superior a 4 KB, debe evaluar la capacidad de la aplicación para controlar este escenario antes de usar ese valor. De lo contrario, debe considerar la posibilidad de usar un tamaño de sector físico redondeado a 4 KB.

El uso de esta IOCTL para obtener el tamaño del sector físico tiene varias limitaciones:

-   Requiere privilegios elevados. Si la aplicación no se ejecuta con privilegios, es posible que tenga que escribir una Windows servicio como se indicó anteriormente.

-   No admite volúmenes SMB. También es posible que tenga que escribir una aplicación Windows servicio para admitir consultas de tamaño de sector físico en estos volúmenes.

-   No se puede emitir a ningún identificador de archivo (la IOCTL debe emitirse a un identificador de volumen).

-   Solo se admite en Windows versiones enumeradas cerca del principio de este artículo.

**Los registros de confirmación se agregan a sectores de 512 bytes**

Las aplicaciones con un almacén de datos suelen tener algún tipo de registro de confirmación que mantiene información sobre los cambios de metadatos o mantiene la estructura del almacén de datos. Para asegurarse de que la pérdida de un sector no afecta a varios registros, este registro de confirmación normalmente se agrega a un tamaño de sector. Con un disco con un tamaño de sector físico mayor, la aplicación deberá consultar el tamaño del sector físico como se muestra en la sección anterior y asegurarse de que cada registro de confirmación se agrega a ese tamaño. Esto no solo evita el ciclo de lectura,modificación y escritura, sino que ayuda a garantizar que, en caso de que se pierda un sector físico, solo se perdería un registro de confirmación.

**Los archivos de registro se escriben en fragmentos no alineados**

La E/S sin búfer se usa normalmente al actualizar o anexar a un archivo de registro. Hay varias maneras de ayudar a garantizar que estas actualizaciones están correctamente alineadas:

-   Internamente, se actualiza el registro de búfer en el tamaño del sector físico notificado de los medios operativos y se emiten escrituras de registro solo cuando una unidad de sector físico está llena.
-   Uso de E/S en búfer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: Formatos de archivo que se basan en sectores de 512 bytes

Algunas aplicaciones con formatos de archivo estándar (como VHD 1.0) pueden tener estos archivos codificados de forma hard para asumir un tamaño de sector de 512 bytes. Por lo tanto, las actualizaciones y escrituras en este archivo darían lugar a un ciclo de lectura,modificación y escritura en el dispositivo, lo que podría dar lugar a problemas de rendimiento y resistencia para los clientes. Sin embargo, hay maneras de que una aplicación proporcione compatibilidad para funcionar en este tipo de medios, por ejemplo:

-   Use el almacenamiento en búfer para asegurarse de que las escrituras se realizan en unidades del tamaño del sector físico.
-   Implemente una lectura-modificación-escritura interna que pueda ayudar a garantizar que las actualizaciones se realizan en unidades del tamaño del sector físico notificado.
-   Si es posible, el relleno registra un sector físico, de forma que el relleno se interpretaría como espacio vacío.
-   Considere la posibilidad de rediseñar una nueva versión de la estructura de datos de la aplicación con compatibilidad con sectores más grandes.

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: El tamaño del sector físico notificado puede cambiar entre sesiones

Hay muchos escenarios en los que el tamaño del sector físico notificado del almacenamiento subyacente que hospeda Datastor puede cambiar. El más común es cuando migra Datastor a otro volumen, o incluso a través de la red. Un cambio en el tamaño del sector físico notificado puede ser un evento inesperado para muchas aplicaciones y puede dar lugar a que algunas aplicaciones incluso no se puedan volver a inicializar.

Este no es el escenario más fácil de admitir y se menciona aquí como un aviso. Debe tener en cuenta los requisitos de movilidad de los clientes y ajustar el soporte técnico en consecuencia para ayudar a garantizar que los clientes no se verán afectados negativamente mediante el uso de medios 512e.

## <a name="4-kb-native-media"></a>Medios nativos de 4 KB

Los medios de emulación de 512 bytes están pensados como un paso transitorio entre medios nativos de 512 bytes y medios nativos de 4 KB, y esperamos ver 4 medios nativos de KB publicados poco después de que 512e esté disponible. Hay varias implicaciones importantes con este medio que se deben tener en cuenta:

-   Los tamaños de sector lógico y físico son de 4 KB.
-   Dado que no hay ninguna capa de emulación, el almacenamiento no podrá realizar las escrituras no alineadas.
-   No se ha alcanzado la resistencia oculta: las aplicaciones funcionan o no funcionan

Aunque Microsoft está investigando actualmente la compatibilidad con estos tipos de medios en una versión futura de Windows y emitirá un artículo de KB cuando corresponda, los desarrolladores de aplicaciones deben considerar la posibilidad de proporcionar soporte técnico preferentemente para estos tipos de medios.

## <a name="closing"></a>Cierre

En este artículo se han analizado las afectaciones que los medios de sector de gran tamaño presentan con muchos escenarios de implementación comunes. Hemos visto el impacto en el rendimiento y la resistencia de read-modify-write, algunos de los escenarios interesantes que puede presentar este medio y el conjunto de problemas que pueden provocar con el software, lo que en última instancia afecta al usuario final. El sector de almacenamiento está cambiando rápidamente a medios con tamaños de sector más grandes y muy pronto los clientes no podrán comprar discos con tamaños tradicionales de sector de 512 bytes.

Se trata de un documento vivo y está pensado como ayuda para que los desarrolladores puedan comprender esta transición. Debe iniciar una conversación con sus respectivas organizaciones, con clientes, profesionales de TI y proveedores de hardware para hablar sobre la transición de sector grande y cómo afecta a los escenarios que son importantes para usted.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   **Windows de soporte técnico general:**<https://support.microsoft.com/kb/2510009>
-   **Revisión para Windows 7 y Windows Server 2008 R2:**<https://support.microsoft.com/kb/982018>
-   **Revisión para Windows Vista y Windows Server 2008:**<https://support.microsoft.com/kb/2470478>
-   **Instrucción de compatibilidad de HyperV:**<https://support.microsoft.com/kb/2515143>
-   **Información general sobre IOCTL \_ Código de control STORAGE \_ QUERY \_ PROPERTY**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ Código \_ de control STORAGE QUERY \_ PROPERTY**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Información general sobre STORAGE \_ ESTRUCTURA DESCRIPTOR \_ DE \_ ALINEACIÓN DE ACCESO:**[https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descripción de la terminología estándar que se usa para describir las actualizaciones de software de Microsoft:**<https://support.microsoft.com/kb/824684/>
-   Código de ejemplo **de WDK** con detalles sobre cómo extraer la información de alineación de acceso de almacenamiento notificada de la estructura **\_ \_ \_ DESCRIPTOR** DE ALINEACIÓN DE ACCESO DE ALMACENAMIENTO al realizar una llamada al código de control **IOCTL STORAGE QUERY \_ \_ \_ PROPERTY:** [/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Información general sobre ImageX Command-Line opciones**:<https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisitos del controlador Intel Intel Chips para admitir unidades de sector de 4 KB:**<https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Para más información sobre los discos de formato avanzado, visite los siguientes sitios web de IDEMA:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
