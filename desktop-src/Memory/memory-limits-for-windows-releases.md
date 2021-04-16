---
description: En este tema se describen los límites de memoria para las versiones compatibles de Windows y Windows Server.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Memory Limits for Windows and Windows Server Releases (Límites de memoria para versiones de Windows y Windows Server)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09db7d303468247794807629d3a56e786c4ada6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678531"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Memory Limits for Windows and Windows Server Releases (Límites de memoria para versiones de Windows y Windows Server)

En este tema se describen los límites de memoria para las versiones compatibles de Windows y Windows Server.

-   [Límites de espacio de direcciones y memoria](#memory-limits-for-windows-and-windows-server-releases)
-   [Límites de memoria física: Windows 10](#physical-memory-limits-windows-10)
-   [Límites de memoria física: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Límites de memoria física: Windows 8](#physical-memory-limits-windows-8)
-   [Límites de memoria física: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Límites de memoria física: Windows 7](#physical-memory-limits-windows-7)
-   [Límites de memoria física: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Límites de memoria física: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Límites de memoria física: Windows Vista](#physical-memory-limits-windows-vista)
-   [Límites de memoria física: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Límites de memoria física: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Límites de memoria física: Windows Server 2003 con Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Límites de memoria física: Windows Server 2003 con Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Límites de memoria física: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Límites de memoria física: Windows XP](#physical-memory-limits-windows-xp)
-   [Límites de memoria física: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Cómo afectan a los límites de memoria las tarjetas de gráficos y otros dispositivos](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Temas relacionados](#related-topics)

Los límites en la memoria y el espacio de direcciones varían según la plataforma, el sistema operativo y si el valor de **archivo de imagen de \_ \_ gran tamaño con \_ \_ reconocimiento de direcciones** de la estructura de la [**\_ imagen cargada**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) y la [optimización de 4 gigabytes](4-gigabyte-tuning.md) (4GT) están en uso. **Imagen \_ de La \_ \_ \_ identificación de la dirección grande del archivo** se establece o se borra mediante la opción del vinculador [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) .

la optimización de 4 gigabytes (4GT), también conocida como optimización de la memoria de la aplicación o el modificador/3GB, es una tecnología (solo aplicable a sistemas de 32 bits) que altera la cantidad de espacio de direcciones virtuales disponible para las aplicaciones en modo de usuario. Al habilitar esta tecnología se reduce el tamaño total del espacio de direcciones virtuales del sistema y, por lo tanto, los recursos del sistema son máximos. Para obtener más información, consulte [¿Qué es 4GT]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))?

Los límites de la memoria física para las plataformas de 32 bits también dependen de la [extensión de dirección física](physical-address-extension.md) (PAE), que permite a los sistemas Windows de 32 bits usar más de 4 GB de memoria física.

## <a name="memory-and-address-space-limits"></a>Límites de espacio de direcciones y memoria

En la tabla siguiente se especifican los límites de memoria y espacio de direcciones para las versiones compatibles de Windows. A menos que se indique lo contrario, los límites de esta tabla se aplican a todas las versiones admitidas.



| Tipo de memoria                                                                                   | Límite en x86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Límite en Windows de 64 bits                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espacio de direcciones virtuales en modo de usuario para cada proceso de 32 bits<br/>                            | 2 GB<br/> Hasta 3 GB con un **archivo de imagen de \_ \_ gran tamaño con \_ \_ reconocimiento de direcciones** y 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB con **archivo de imagen con \_ \_ \_ \_ reconocimiento de dirección grande** desactivado (valor predeterminado)<br/> 4 GB con un **archivo de imagen de \_ \_ gran tamaño con \_ \_ reconocimiento de direcciones**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Espacio de direcciones virtuales en modo de usuario para cada proceso de 64 bits<br/>                            | No aplicable<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Con imagen \_ Conjunto de archivos con \_ \_ \_ reconocimiento de direcciones grandes** (valor predeterminado):<br/> **x64: Windows 8.1 y Windows Server 2012 R2 o posterior:** 128 TB<br/> **x64: Windows 8 y Windows Server 2012 o versiones anteriores de** 8 TB<br/> **Sistemas basados en Itanium de Intel:** 7 TB<br/> <br/> 2 GB con **archivo de imagen con \_ \_ \_ \_ reconocimiento de dirección grande** desactivado<br/>                                                                                                                                                                                              |
| Espacio de direcciones virtuales en modo kernel<br/>                                                  | 2 GB<br/> De 1 GB a un máximo de 2 GB con 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 y Windows Server 2012 R2 o posterior:** 128 TB<br/> **Windows 8 y Windows Server 2012 o versiones anteriores de** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Grupo paginado<br/>                                                                         | 384 GB o límite de confirmación del sistema, el que sea menor. **Windows 8.1 y Windows Server 2012 R2:** 15,5 TB o límite de confirmación del sistema, lo que sea menor. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Limitado por el espacio de direcciones virtuales en modo kernel disponible. A partir de Windows Vista con Service Pack 1 (SP1), el grupo paginado también puede estar limitado por el valor de la clave del registro [PagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server y Windows Server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB o límite de confirmación del sistema, lo que sea más pequeño **Windows 8.1 y Windows Server 2012 R2:** 15,5 TB o límite de confirmación del sistema, el que sea menor. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** 128 GB o límite de confirmación del sistema, lo que sea menor<br/> **Windows Server 2003 y Windows XP:** Hasta 128 GB según la configuración y la RAM.<br/> <br/>                                                                                |
| Bloque no paginado<br/>                                                                      | 75% de RAM o 2 GB, lo que sea menor. **Windows 8.1 y Windows Server 2012 R2:** RAM o 16 TB, lo que sea menor (el espacio de direcciones está limitado a 2 x RAM).<br/> **Windows Vista:** Limitado solo por el espacio de direcciones virtuales del modo kernel y la memoria física. A partir de Windows Vista con SP1, el grupo no paginado también puede estar limitado por el valor de la clave del registro [NonPagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows Server 2003 y Windows XP:** 256 mb o 128 MB con 4GT.<br/> <br/>                                                                                                                                                 | RAM o 128 GB, lo que sea menor (el espacio de direcciones está limitado a 2 x RAM) **Windows 8.1 y Windows Server 2012 R2:** RAM o 16 TB, el que sea menor (el espacio de direcciones está limitado a 2 x RAM).<br/> **Windows server 2008 R2, Windows 7 y Windows server 2008:** 75% de RAM hasta un máximo de 128 GB<br/> **Windows Vista:** 40% de la RAM hasta un máximo de 128 GB.<br/> **Windows Server 2003 y Windows XP:** Hasta 128 GB según la configuración y la RAM.<br/> <br/> |
| Espacio de direcciones virtuales de caché del sistema (tamaño físico limitado solo por la memoria física)<br/> | Limitado por el espacio de direcciones virtuales en modo kernel disponible o por el valor de la clave del registro [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows 8.1 y Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Limitado solo por el espacio de direcciones virtuales del modo kernel. A partir de Windows Vista con SP1, el espacio de direcciones virtuales de caché del sistema también puede estar limitado por el valor de la clave del registro [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows Server 2003 y Windows XP:** 860 MB con el conjunto de claves del registro [LARGESYSTEMCACHE](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) y sin 4GT; hasta 448 MB con 4GT.<br/> <br/> | Siempre es 1 TB independientemente de la RAM física **Windows 8.1 y Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 y Windows XP:** Hasta 1 TB según la configuración y la RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Límites de memoria física: Windows 10

En la tabla siguiente se especifican los límites de la memoria física para Windows 10.



| Versión               | Límite en x86    | Límite en x64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Límites de memoria física: Windows Server 2016

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2016.



| Versión                        | Límite en x64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Límites de memoria física: Windows 8

En la tabla siguiente se especifican los límites de la memoria física para Windows 8.



| Versión                | Límite en x86    | Límite en x64      |
|------------------------|-----------------|-------------------|
| Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Límites de memoria física: Windows Server 2012

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2012. Windows Server 2012 solo está disponible en las ediciones x64.



| Versión                               | Límite en x64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Límites de memoria física: Windows 7

En la tabla siguiente se especifican los límites de la memoria física para Windows 7.



| Versión                | Límite en x86    | Límite en x64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | N/D<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Límites de memoria física: Windows Server 2008 R2

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2008 R2. Windows Server 2008 R2 solo está disponible en las ediciones de 64 bits.



| Versión                                          | Límite en x64      | Límite en IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 for Itanium-Based Systems |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Límites de memoria física: Windows Server 2008

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2008. Los límites superiores a 4 GB para Windows de 32 bits suponen que [PAE](physical-address-extension.md) está habilitado.



| Versión                                       | Límite en x86     | Límite en x64      | Límite en IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 for Itanium-Based Systems |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Límites de memoria física: Windows Vista

En la tabla siguiente se especifican los límites de la memoria física para Windows Vista.



| Versión                    | Límite en x86    | Límite en x64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Límites de memoria física: Windows Home Server

Windows Home Server solo está disponible en una edición de 32 bits. El límite de memoria física es 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Límites de memoria física: Windows Server 2003 R2

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2003 R2. Los límites de más de 4 GB para Windows de 32 bits suponen que [PAE](physical-address-extension.md) está habilitado.



| Versión                                              | Límite en x86                                 | Límite en x64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Límites de memoria física: Windows Server 2003 con Service Pack 2 (SP2)

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2003 con Service Pack 2 (SP2). Los límites de más de 4 GB para Windows de 32 bits suponen que [PAE](physical-address-extension.md) está habilitado.



| Versión                                                                      | Límite en x86                                 | Límite en x64     | Límite en IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 con Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Límites de memoria física: Windows Server 2003 con Service Pack 1 (SP1)

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2003 con Service Pack 1 (SP1). Los límites de más de 4 GB para Windows de 32 bits suponen que [PAE](physical-address-extension.md) está habilitado.



| Versión                                                                      | Límite en x86                                 | Límite en x64        | Límite en IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 con Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 64 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 64 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Límites de memoria física: Windows Server 2003

En la tabla siguiente se especifican los límites de la memoria física para Windows Server 2003. Los límites de más de 4 GB para Windows de 32 bits suponen que [PAE](physical-address-extension.md) está habilitado.



| Versión                                                    | Límite en x86                                 | Límite en IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003, Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Storage Server 2003, Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Límites de memoria física: Windows XP

En la tabla siguiente se especifican los límites de la memoria física para Windows XP.



| Versión                    | Límite en x86      | Límite en x64      | Límite en IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (no compatible)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/D<br/>    | N/D<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Límites de memoria física: Windows Embedded

En la tabla siguiente se especifican los límites de la memoria física para Windows Embedded.



| Versión                                   | Límite en x86    | Límite en x64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Cómo afectan a los límites de memoria las tarjetas de gráficos y otros dispositivos

Los dispositivos deben asignar su memoria por debajo de 4 GB por compatibilidad con las versiones de Windows no compatibles con PAE. Por lo tanto, si el sistema tiene 4 GB de RAM, algunos de ellos están deshabilitados o se reasignan por encima de 4 GB por el BIOS. Si se reasigna la memoria, Windows x64 puede usar esta memoria. Las versiones de cliente x86 de Windows no admiten la memoria física por encima de la marca de 4 GB, por lo que no pueden tener acceso a estas regiones reasignadas. Cualquier versión x64 de Windows o x86 Server puede.

Las versiones de cliente x86 con PAE habilitado tienen un espacio de direcciones físicas de 37 bits (128 GB) utilizable. El límite que imponen estas versiones es la dirección de RAM física más alta permitida, no el tamaño del espacio de e/s. Esto significa que los controladores compatibles con PAE pueden utilizar realmente espacio físico por encima de 4 GB si lo desean. Por ejemplo, los controladores podrían asignar las regiones de memoria "perdidas" que se encuentran por encima de 4 GB y exponer esta memoria como un disco RAM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Optimización de 4 gigabytes](4-gigabyte-tuning.md)
</dt> <dt>

[**\_reconocimiento de \_ \_ dirección grande de archivo \_ de imagen**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Extensión de dirección física](physical-address-extension.md)
</dt> </dl>

 

 
