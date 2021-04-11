---
description: Describe las consideraciones para el control de aplicaciones del almacenamiento en búfer de archivos, también conocido como entrada/salida (e/s) de archivo no almacenado en búfer.
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: Almacenamiento en búfer de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278820"
---
# <a name="file-buffering"></a>Almacenamiento en búfer de archivo

En este tema se tratan las distintas consideraciones para el control de aplicaciones del almacenamiento en búfer de archivos, también conocido como entrada/salida (e/s) de archivo no almacenado en búfer. El almacenamiento en búfer de archivos normalmente lo controla el sistema en segundo plano y se considera parte del [almacenamiento en caché](file-caching.md) de archivos dentro del sistema operativo Windows, a menos que se especifique lo contrario. Aunque los términos *almacenamiento en caché y almacenamiento en* *búfer* se usan a veces indistintamente, en este tema se usa el término *almacenamiento en búfer* específicamente en el contexto de explicar cómo interactuar con los datos que no están almacenados en caché (almacenados en búfer) por el sistema, donde se encuentra en gran medida del control directo de las aplicaciones en modo usuario.

Al abrir o crear un archivo con la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , la marca de **archivo sin marca de almacenamiento en \_ \_ \_ búfer** puede especificarse para deshabilitar el almacenamiento en caché del sistema de los datos que se leen o se escriben en el archivo. Aunque esto proporciona un control directo y completo sobre el almacenamiento en búfer de e/s de datos, en el caso de archivos y dispositivos similares, se deben tener en cuenta los requisitos de alineación de datos.

> [!Note]  
> Esta información de alineación se aplica a la e/s en dispositivos tales como archivos que admiten búsquedas y el concepto de punteros de posición de archivo (o *desplazamientos*). En el caso de los dispositivos que no buscan, como canalizaciones con nombre o dispositivos de comunicaciones, la desactivación del almacenamiento en búfer puede no requerir ninguna alineación determinada. Las limitaciones o eficiencias que se puedan obtener mediante la alineación en ese caso dependen de la tecnología subyacente.

 

En un ejemplo simple, la aplicación abriría un archivo para el acceso de escritura con la marca de **archivo sin marca de \_ almacenamiento en \_ \_ búfer** y, a continuación, realiza una llamada a la función [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) mediante un búfer de datos definido en la aplicación. Este búfer local es, en estas circunstancias, el único búfer de archivo que existe para esta operación. Debido a la distribución del disco físico, al diseño de almacenamiento del sistema de archivos y al seguimiento de la posición del puntero de archivo de nivel de sistema, esta operación de escritura producirá un error a menos que los búferes de datos definidos localmente cumplan determinados criterios de alineación, que se describen en la sección siguiente.

> [!Note]  
> La explicación del almacenamiento en caché no tiene en cuenta el almacenamiento en caché del hardware en el disco físico, que no se garantiza que esté dentro del control directo del sistema en ningún caso. Esto no tiene ningún efecto en los requisitos especificados en este tema.

 

Para obtener más información sobre cómo la **marca de archivo \_ \_ sin \_ almacenamiento en búfer** interactúa con otras marcas relacionadas con la memoria caché, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

## <a name="alignment-and-file-access-requirements"></a>Requisitos de alineación y acceso a archivos

Como se explicó anteriormente, una aplicación debe cumplir ciertos requisitos al trabajar con archivos abiertos **con \_ marca de archivo \_ sin almacenamiento en \_ búfer**. Se aplican las siguientes características:

-   Los tamaños de acceso a archivos, incluido el desplazamiento opcional de archivo en la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , si se especifica, deben ser para un número de bytes que sea un entero múltiplo del tamaño del sector del volumen. Por ejemplo, si el tamaño del sector es de 512 bytes, una aplicación puede solicitar lecturas y escrituras de 512, 1.024, 1.536 o 2.048 bytes, pero no de 335, 981 o 7.171 bytes.
-   Las direcciones de búfer de acceso a archivos para las operaciones de lectura y escritura deben estar alineadas con el sector físico, lo que significa que están alineadas en las direcciones en memoria que son múltiplos enteros del tamaño de sector físico del volumen. En función del disco, es posible que no se aplique este requisito.

Los desarrolladores de aplicaciones deben tener en cuenta los nuevos tipos de dispositivos de almacenamiento que se incorporan en el mercado con un tamaño de sector de medios físicos de 4.096 bytes. El nombre del sector de estos dispositivos es "Advanced Format". Como puede haber problemas de compatibilidad con la introducción directa de 4.096 bytes como unidad de direccionamiento para los medios, una solución de compatibilidad temporal consiste en introducir dispositivos que emulen un dispositivo de almacenamiento del sector de 512 bytes normal, pero que ofrecen información disponible sobre el verdadero tamaño del sector a través de los comandos estándar de ATA y SCSI.

Como resultado de esta emulación, en esencia hay dos tamaños de sector que los desarrolladores deben conocer:

-   Sector lógico: unidad que se usa para el direccionamiento de bloque lógico para los medios. También podemos considerarla como la unidad más pequeña de escritura que el almacenamiento puede aceptar. Esta es la "emulación".
-   Sector físico: unidad para la que se completan las operaciones de lectura y escritura en el dispositivo en una sola operación. Se trata de la unidad de escritura atómica y de qué e/s no almacenada en búfer necesitará alinearse con el fin de tener características de confiabilidad y rendimiento óptimas.

La mayoría de las API de Windows actuales, como [**ioctl \_ Disk \_ Get \_ Drive \_ Geometry**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry) y [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea), devolverán el tamaño del sector lógico, pero el tamaño del sector físico se puede recuperar a través del código de control de [**\_ propiedad de \_ consulta \_ de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) , con la información pertinente contenida en el miembro **BytesPerPhysicalSector** en la estructura del [**\_ \_ \_ descriptor de alineación de acceso de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) . Para obtener un ejemplo, vea el código de ejemplo en el [**\_ \_ \_ descriptor de alineación de acceso al almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor). Microsoft recomienda encarecidamente que los desarrolladores alineen la e/s no almacenada en búfer con el tamaño de sector físico, tal y como lo indique el código de control de **\_ propiedad de \_ consulta \_ de almacenamiento ioctl** para ayudar a garantizar que sus aplicaciones estén preparadas para esta transición de tamaño de sector.

**Windows Server 2003 y Windows XP:** La estructura del [**\_ \_ \_ descriptor de alineación de acceso de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) no está disponible. Se presentó con Windows Vista y Windows Server 2008.

Dado que las direcciones de búfer para las operaciones de lectura y escritura deben estar alineadas por sectores, la aplicación debe tener control directo sobre cómo se asignan estos búferes. Una manera de utilizar los búferes de alineación de sectores es usar la función [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) para asignar los búferes. Tenga en cuenta lo siguiente.

-   [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) asigna memoria que está alineada en direcciones que son múltiplos enteros del tamaño de página del sistema. El tamaño de página es de 4.096 bytes en x64 y en bytes x86 o 8.192 para sistemas basados en Itanium. Para obtener más información, vea la función [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .
-   El tamaño del sector suele ser de 512 a 4.096 bytes para dispositivos de almacenamiento de acceso directo (discos duros) y 2.048 bytes para CD-ROM.
-   Los tamaños de página y de sector son potencias de 2.

Por lo tanto, en la mayoría de los casos, la memoria alineada en páginas también estará alineada por sectores, porque el caso en el que el tamaño del sector es mayor que el tamaño de página es poco frecuente.

Otra manera de obtener los búferes de memoria alineados manualmente es usar la función [ \_ aligned \_ malloc](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019) de la biblioteca de Run-Time de C. Para obtener un ejemplo de cómo controlar manualmente la alineación del búfer, vea el ejemplo de código del lenguaje C++ en la sección de código de ejemplo de [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile).

 

 
