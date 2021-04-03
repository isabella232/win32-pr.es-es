---
description: En este tema se presenta el efecto de los dispositivos de almacenamiento de formato avanzado en el software, se describen las aplicaciones que pueden hacer para ayudar a admitir este tipo de medios y se describe la infraestructura que Microsoft incorporó con Windows 7 SP1 y Windows Server 2008 R2 SP1 para permitir que los desarrolladores admitan estos tipos de dispositivos.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Actualización de compatibilidad de disco de emulación de 512 bytes (512e)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fbdce2937e2d121d892d8566755dfcb7f20f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083425"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Actualización de compatibilidad de disco de emulación de 512 bytes (512e)

## <a name="platform"></a>Plataforma

 **Clientes** : Windows Vista Windows \| 7 Windows \| 7 SP1  
**Servidores** : windows Server 2008 \| Windows Server 2008 r2 \| Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Impacto en las características

**Gravedad** alta  
**Frecuencia** : alta  









## <a name="description"></a>Descripción

Las densidades geométricas son cada vez mayores y, con la reciente llegada de discos de 3 TB, los mecanismos de corrección de errores que se usan para tratar la decreciente relación señal-ruido (SNR) se están convirtiendo en un espacio ineficaz, es decir, se requiere una mayor cantidad de sobrecarga para asegurarse de que se pueda usar el medio. Una de las soluciones del sector de almacenamiento para mejorar este mecanismo de corrección de errores consiste en introducir un formato de medios físicos diferente que incluye un tamaño de sector físico mayor. Este nuevo formato de medio físico se denomina *formato avanzado*. Por lo tanto, ya no es seguro hacer ninguna suposición con respecto al tamaño de sector de los dispositivos de almacenamiento modernos y los desarrolladores deberán estudiar las suposiciones subyacentes a su código para determinar si hay un impacto.

En este tema se presenta el efecto de los dispositivos de almacenamiento de formato avanzado en el software, se describen las aplicaciones que pueden hacer para ayudar a admitir este tipo de medios y se describe la infraestructura para permitir que los desarrolladores admitan estos tipos de dispositivos. Aunque el material presentado en este tema proporciona directrices para mejorar la compatibilidad con los discos con formato avanzado, la información se aplica generalmente a todos los sistemas con discos con formato avanzado. Las siguientes versiones de Windows proporcionan compatibilidad para consultar el tamaño del sector físico:

-   Windows 7 con Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Para obtener más información, consulte la [información sobre la Directiva de soporte técnico de Microsoft para unidades de sector grande en Windows](https://support.microsoft.com/kb/2510009).

Para obtener más información acerca de los discos con formato avanzado, póngase en contacto con su proveedor de almacenamiento.

## <a name="logical-vs-physical-sector-size"></a>En comparación con el tamaño de sector físico

Una de las preocupaciones de la introducción de este cambio en el formato multimedia es la compatibilidad con el software y el hardware actualmente disponibles en el mercado hoy en día. Como solución temporal, el sector de almacenamiento está introduciendo inicialmente discos que emulan un disco de sector de 512 bytes normal, pero facilitan la información disponible sobre el tamaño de sector real a través de los comandos estándar de ATA y SCSI. Como resultado de esta emulación, hay dos tamaños de sector:

-   **Sector lógico**: unidad que se usa para el direccionamiento de bloque lógico para los medios. También podemos considerarla como la unidad más pequeña de escritura que el almacenamiento puede aceptar. Esta es la emulación.

-   **Sector físico**: unidad para la que se completan las operaciones de lectura y escritura en el dispositivo en una sola operación. Esta es la unidad de escritura atómica.

La mayoría de las API de Windows actuales, como **ioctl \_ Disk \_ Get \_ Drive \_ Geometry** devolverán el tamaño del sector lógico, pero el tamaño del sector físico se puede recuperar a través del código de control de [ \_ propiedad de \_ consulta \_ de almacenamiento ioctl](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) , con la información pertinente contenida en el campo **BytesPerPhysicalSector** de la estructura del [ \_ \_ \_ descriptor de alineación de acceso de almacenamiento](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) . Esto se describe con más detalle más adelante en el artículo.

## <a name="initial-types-of-large-sector-media"></a>Tipos iniciales de medios de sectores grandes

El sector del almacenamiento es rápidamente el trabajo de transición a este nuevo tipo de formato avanzado de almacenamiento para medios con tamaños de sector físico de 4 KB. Se publicarán dos tipos de medios en el mercado:

-   **4 KB nativo**: este medio no tiene ninguna capa de emulación y expone directamente 4 KB como su tamaño de sector físico y lógico. Este medio no es compatible actualmente con Windows ni con la mayoría de los demás sistemas operativos. Sin embargo, Microsoft está llevando a cabo una investigación sobre la viabilidad de admitir este tipo de medios en una versión futura de Windows y emitirá un artículo de Knowledge base cuando sea apropiado.
-   **emulación de 512 bytes (512e)**: este medio tiene un nivel de emulación como se describe en la sección anterior y expone 512-bytes como su tamaño de sector lógico (similar a un disco normal hoy), pero hace que su información de tamaño de sector físico (4 KB) esté disponible. Esto es lo que varios proveedores de almacenamiento están introduciendo actualmente en el mercado. Este problema general con este nuevo tipo de medios es que la mayoría de las aplicaciones y los sistemas operativos no entienden la existencia del tamaño del sector físico, lo que puede dar lugar a una serie de problemas, como se explica a continuación.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Cómo funciona la emulación: lectura, modificación y escritura (RMW)

Un medio de almacenamiento tiene una unidad determinada en la que se puede modificar el medio físico. Es decir, los medios solo se pueden escribir o volver a escribir en unidades del tamaño de sector físico. Por lo tanto, las operaciones de escritura que no se realicen en este nivel de unidad necesitarán pasos adicionales, que se tratarán en el ejemplo siguiente.

En este escenario, una aplicación necesita actualizar el contenido de un registro de Stor ubicado en un sector lógico de 512 bytes. En el diagrama siguiente se muestran los pasos necesarios para que el dispositivo de almacenamiento complete la escritura:

![pasos necesarios para actualizar el registro de Stor en un sector lógico de 512 bytes](images/512ermwsteps.png)

Como se muestra arriba, este proceso implica algún trabajo por parte del dispositivo de almacenamiento que puede provocar una pérdida de rendimiento. Para evitar este trabajo adicional, las aplicaciones deben actualizarse para hacer lo siguiente:

-   Consultar el tamaño del sector físico.
-   Asegúrese de que las escrituras se alineen con el tamaño de sector físico indicado.

## <a name="the-resiliency-impact-of-read-modify-write"></a>Impacto de resistencia de lectura-modificación-escritura

Las conferencias de resistencia de la capacidad de una aplicación para recuperar el estado entre sesiones. Hemos detectado lo que es necesario para que un dispositivo de almacenamiento de 512e realice una escritura de sectores de 512 bytes: el ciclo de lectura-modificación-escritura. Echemos un vistazo a lo que sucedería si se interrumpiera el proceso de sobrescribir el sector físico anterior en el medio. ¿Cuáles son las consecuencias?

-   Dado que la mayoría de las unidades de disco duro se actualizan en su lugar, el sector físico, es decir, la parte del medio donde se encontraba el sector físico, podría haberse dañado con información incompleta debido a una sobrescritura parcial. Además, puede pensar en ello como si hubiera perdido los 8 sectores lógicos (que el sector físico contiene lógicamente).

-   Aunque la mayoría de las aplicaciones con un almacén de datos están diseñadas con la capacidad de recuperarse de errores de medios, de la pérdida de ocho sectores o de otro modo, la pérdida de ocho registros de confirmación, puede hacer imposible que el almacén de datos se recupere correctamente. Es posible que un administrador tenga que restaurar manualmente la base de datos a partir de una copia de seguridad o incluso puede tener que realizar una regeneración larga.

-   Un impacto más importante es que el acto de otra aplicación que produce un ciclo de lectura-modificación-escritura puede provocar que se pierdan los datos, incluso si la aplicación no se está ejecutando. Esto se debe a que los datos y los datos de la otra aplicación pueden encontrarse en el mismo sector físico.

Teniendo esto en cuenta, es importante que el software de aplicación vuelva a evaluar las suposiciones tomadas en el código y tenga en cuenta la distinción de tamaño de sector físico lógico, junto con algunos escenarios de cliente interesantes que se describen más adelante en este artículo.

Es más probable que este problema se produzca si la aplicación se basa en un almacén de datos de estructura de registro.

## <a name="avoiding-read-modify-write"></a>Evitar la lectura y la escritura

Aunque algunos proveedores de almacenamiento pueden estar introduciendo algunos niveles de mitigación en determinados dispositivos de almacenamiento de 512e para probar y ayudar a facilitar los problemas de rendimiento y resistencia del ciclo de lectura/modificación-escritura, solo hay muchas mitigaciones que pueden controlar en términos de carga de trabajo. Como tal, las aplicaciones no deben basarse en esta mitigación como una solución a largo plazo.

La solución a esto no es una mitigación en el disco, pero para que las aplicaciones realicen el conjunto adecuado de cosas para evitar el ciclo de lectura-modificación-escritura. En esta sección se describen escenarios comunes en los que las aplicaciones pueden tener problemas con discos de sector grande y se sugiere una vía de investigación para probar y resolver cada problema.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problema 1: la partición no está alineada con un límite de sector físico

Cuando el administrador o el usuario crea particiones en el disco, es posible que la primera partición no se haya creado en un límite alineado. Esto puede hacer que todas las escrituras posteriores se desalineen en los límites del sector físico. A partir de Windows Vista SP1 y Windows Server 2008, la primera partición se coloca en los primeros 1024 KB del disco (para discos de 4 GB o más, de lo contrario, la alineación es de 64 KB) que está alineada con un límite de sector físico de 4 KB. Sin embargo, dada la partición predeterminada en Windows XP, una utilidad de creación de particiones de terceros o un uso incorrecto de las API de Windows, es posible que las particiones creadas no estén alineadas con un límite de sector físico. Los desarrolladores deberán asegurarse de que se usan las API correctas para ayudar a garantizar la alineación. Las API recomendadas para ayudar a garantizar la alineación de la partición se describen a continuación.

Las API **IVdsPack:: CreateVolume** y **IVdsPack2:: CreateVolume2** no usan el parámetro de alineación especificado cuando se crea un nuevo volumen y, en su lugar, usan el valor predeterminado de alineación para el sistema operativo (anterior a windows Vista SP1 usará 63 bytes y después Windows Vista SP1 usará los valores predeterminados indicados anteriormente). Por lo tanto, se recomienda que las aplicaciones que necesitan crear particiones usen las API **IVdsCreatePartitionEx:: CreatePartitionEx** o **IVdsAdvancedDisk:: CreatePartition** en su lugar, que usan el parámetro de alineación especificado.

La mejor manera de asegurarse de que la alineación sea correcta es hacerlo bien cuando se crea la partición inicialmente. En caso contrario, la aplicación deberá tener en cuenta la alineación al realizar operaciones de escritura o de inicialización, lo que puede ser una cuestión muy compleja. A partir de Windows Vista SP1, no suele ser un problema; sin embargo, las versiones anteriores de Windows pueden crear particiones no alineadas que podrían provocar problemas de rendimiento con algunos discos de formato avanzado.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problema 2: Escrituras no almacenadas en búfer no alineadas con el tamaño de sector físico

El problema básico es que las escrituras no almacenadas en búfer no se alinean con el tamaño de sector físico indicado de los medios de almacenamiento, lo que desencadena una lectura-modificación-escritura en la unidad que puede producir problemas de rendimiento. Por otro lado, las escrituras almacenadas en búfer se alinean con el tamaño de página (4 KB), que casualmente es el tamaño de sector físico de la primera generación de medios de sector grande. Sin embargo, la mayoría de las aplicaciones con un almacén de datos realizan escrituras no almacenadas en búfer y, por lo tanto, deberán asegurarse de que estas escrituras se realicen en unidades del tamaño de sector físico.

Para ayudar a determinar si la aplicación emite e/s sin almacenamiento en búfer, compruebe que incluye la marca de archivo no incluir marca de **almacenamiento en \_ \_ \_ búfer** en el parámetro *dwFlagsAndAttributes* cuando se llama a la función **CreateFile** .

Además, si está alineando actualmente las escrituras en el tamaño del sector, lo más probable es que este tamaño de sector sea solo el tamaño del sector *lógico* , ya que la mayoría de las API existentes que consultan el tamaño del sector del medio realmente simplemente consultan la unidad de direccionamiento, es decir, el tamaño del sector lógico. El tamaño de sector de interés es el tamaño del sector físico, que es la unidad real de atomicidad. Algunos ejemplos de API que recuperan el tamaño del sector lógico son:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **Ioctl \_ el disco \_ obtiene la \_ \_ geometría de unidad**, el **\_ disco ioctl obtiene la geometría de \_ \_ unidad \_ \_ ex**
-   **IVdsDisk:: GetProperties**, **IVdsDisk3:: GetProperties2**

**Cómo consultar el tamaño del sector físico**

Microsoft ha proporcionado un ejemplo de código en MSDN que detalla cómo una aplicación puede consultar el tamaño del sector físico del volumen. El ejemplo de código se encuentra en <https://msdn.microsoft.com/library/ff800831.aspx> .

Aunque el ejemplo de código anterior le permite obtener el tamaño del sector físico del volumen, debe realizar algunas comprobaciones básicas en el tamaño del sector físico indicado antes de usarlo, ya que es posible que algunos controladores no devuelvan datos con el formato correcto:

-   Asegúrese de que el tamaño de sector físico indicado es >= el tamaño de sector lógico indicado. Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño de sector lógico indicado.
-   Asegúrese de que el tamaño de sector físico indicado sea una potencia de dos. Si no es así, la aplicación debe usar un tamaño de sector físico igual al tamaño de sector lógico indicado.
-   Si el tamaño del sector físico es un valor de potencia de dos entre 512 y 4 KB, debería considerar la posibilidad de usar un tamaño de sector físico redondeado hacia abajo al tamaño del sector lógico indicado.
-   Si el tamaño del sector físico es un valor de potencia de dos superior a 4 KB, debe evaluar la capacidad de la aplicación para controlar este escenario antes de usar ese valor. De lo contrario, debería considerar el uso de un tamaño de sector físico redondeado a 4 KB.

El uso de este IOCTL para obtener el tamaño del sector físico tiene varias limitaciones:

-   Requiere privilegios elevados. Si la aplicación no se ejecuta con privilegios, puede que tenga que escribir una aplicación de servicio de Windows como se indicó anteriormente.

-   No admite volúmenes SMB. También es posible que tenga que escribir una aplicación de servicio de Windows para admitir la consulta de tamaño de sector físico en estos volúmenes.

-   No se puede emitir a ningún identificador de archivo (IOCTL debe emitirse a un identificador de volumen).

-   Solo se admite en las versiones de Windows que se indican cerca del principio de este artículo.

**Los registros de confirmación se rellenan hasta los sectores de 512 bytes**

Normalmente, las aplicaciones con un almacén de datos tienen alguna forma de registro de confirmación que mantiene información sobre los cambios en los metadatos o mantiene la estructura del almacén de datos. Con el fin de garantizar que la pérdida de un sector no afecte a varios registros, este registro de confirmación se rellena normalmente en un tamaño de sector. Con un disco con un tamaño de sector físico mayor, la aplicación tendrá que consultar el tamaño de sector físico tal como se muestra en la sección anterior y asegurarse de que cada registro de confirmación se rellene hasta ese tamaño. Esto no solo evita el ciclo de lectura-modificación-escritura, sino que ayuda a garantizar que, en caso de que se pierda un sector físico, solo se perdería un registro de confirmación.

**Los archivos de registro se escriben en fragmentos no alineados**

La e/s no almacenada en búfer se usa normalmente al actualizar o anexar a un archivo de registro. Hay varias maneras de ayudar a garantizar que estas actualizaciones se alineen correctamente:

-   Almacene internamente las actualizaciones de registro en el tamaño del sector físico indicado del medio operativo y emita escrituras de registro solo cuando una unidad de sector físico esté llena
-   Usar e/s almacenada en búfer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: formatos de archivo que se basan en sectores de 512 bytes

Algunas aplicaciones con formatos de archivo estándar (como VHD 1,0) pueden tener estos archivos codificados de forma rígida para asumir un tamaño de sector de 512 bytes. Por lo tanto, las actualizaciones y escrituras en este archivo darían como resultado un ciclo de lectura-modificación-escritura en el dispositivo, lo que podría dar lugar a problemas de rendimiento y resistencia para los clientes. Sin embargo, hay maneras de que una aplicación proporcione compatibilidad para trabajar en este tipo de medios, por ejemplo:

-   Use el almacenamiento en búfer para asegurarse de que las escrituras se realicen en unidades del tamaño de sector físico
-   Implementar un interno de lectura/modificación-escritura que puede ayudar a garantizar que las actualizaciones se realicen en unidades del tamaño de sector físico indicado
-   Si es posible, rellenar los registros en un sector físico, de tal forma que el relleno se interprete como espacio vacío
-   Considere la posibilidad de volver a diseñar una nueva versión de la estructura de datos de la aplicación compatible con sectores mayores

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: el tamaño del sector físico indicado puede cambiar entre sesiones

Hay muchos escenarios en los que el tamaño de sector físico indicado del almacenamiento subyacente que hospeda el Stor puede cambiar. Lo más común es cuando se migra el Stor a otro volumen, o incluso a través de la red. Un cambio en el tamaño del sector físico indicado puede ser un evento inesperado para muchas aplicaciones y puede dar lugar a que algunas aplicaciones no se reinicialicen.

Este no es el escenario más sencillo de admitir y se menciona aquí como aviso. Debe tener en cuenta los requisitos de movilidad de sus clientes y ajustar su soporte en consecuencia para ayudar a garantizar que los clientes no se vean afectados negativamente mediante el uso de medios 512e.

## <a name="4-kb-native-media"></a>Medios nativos de 4 KB

los medios de emulación de 512 bytes están pensados como un paso transitorio entre los medios nativos de 512 bytes y 4 KB nativos, y esperamos ver que se publican 4 KB nativos en breve después de que 512e esté disponible. Hay varias implicaciones importantes con este medio que se deben anotar:

-   Los tamaños de sector lógico y físico son 4 KB
-   Dado que no hay ninguna capa de emulación, el almacenamiento producirá un error en las escrituras no alineadas.
-   No se ha encontrado ninguna resistencia oculta: las aplicaciones funcionan o no funcionan

Aunque Microsoft está investigando actualmente la compatibilidad con estos tipos de medios en una versión futura de Windows y emitirá un artículo de Knowledge base cuando corresponda, los desarrolladores de aplicaciones deben considerar la posibilidad de proporcionar de forma preferente compatibilidad con estos tipos de medios.

## <a name="closing"></a>Cierre

En este artículo hemos analizado los efectos que presentan los medios del sector grande con muchos escenarios comunes de implementación. Hemos visto el impacto en el rendimiento y la resistencia de Read-Modify-Write, algunos de los escenarios interesantes que este medio puede introducir y el conjunto de problemas que pueden producirse con software, que en última instancia afecta al usuario final. El sector del almacenamiento realiza una transición rápida a los medios con tamaños de sector más grandes y, en breve, los clientes no podrán comprar discos con tamaños de sector de 512 bytes tradicionales.

Se trata de un documento vivo y está pensado como ayuda para que los desarrolladores puedan comprender esta transición. Debe iniciar una conversación con sus organizaciones respectivas, con clientes, profesionales de ti y los proveedores de hardware para hablar sobre la transición del sector grande y cómo afecta a los escenarios que son importantes para usted.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   **Instrucción de soporte general de Windows**: <https://support.microsoft.com/kb/2510009>
-   **Revisión para Windows 7 y Windows Server 2008 R2**: <https://support.microsoft.com/kb/982018>
-   **Revisión para Windows Vista y Windows Server 2008**: <https://support.microsoft.com/kb/2470478>
-   **Declaración de compatibilidad de HyperV**: <https://support.microsoft.com/kb/2515143>
-   **Información general sobre ioctl \_ \_Código de \_ control de propiedad de consulta de almacenamiento**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **Ioctl \_ \_Código de \_ control de propiedad de consulta de almacenamiento**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Información general sobre el almacenamiento \_ \_Estructura del \_ descriptor de alineación de acceso**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descripción de la terminología estándar que se usa para describir las actualizaciones de software de Microsoft**: <https://support.microsoft.com/kb/824684/>
-   **Código de ejemplo de WDK** con detalles sobre cómo extraer la información de alineación de acceso de almacenamiento de la estructura de **\_ \_ \_ descriptor de alineación de acceso de almacenamiento** al realizar una llamada al código de control de la **\_ \_ \_ propiedad de consulta de almacenamiento ioctl** : [/Windows/Desktop/API/winioctl/NS-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Información general sobre las opciones de Command-Line de ImageX**: <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisitos del controlador del chipset Intel para admitir unidades del sector de 4 KB**: <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Para obtener más información sobre los discos con formato avanzado, visite los siguientes sitios web de IDEMA:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
