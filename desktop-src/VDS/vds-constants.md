---
description: Constantes de VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678384"
---
# <a name="vds-constants"></a>Constantes de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Las constantes de VDS se clasifican como se indica a continuación:

-   [Constantes de estado de objetos](#object-status-constants)
-   [Constantes de sugerencias de automagic](#automagic-hints-constants)
-   [Constantes misceláneas](#miscellaneous-constants)

### <a name="object-status-constants"></a>Constantes de estado de objetos



| Constante           | Value |
|--------------------|-------|
| ESTADO \_ desconocido    | 0     |
| ESTADO \_ en línea     | 1     |
| ESTADO \_ no \_ listo | 2     |
| ESTADO \_ sin \_ medios  | 3     |
| ESTADO \_ sin conexión    | 4     |
| error de estado \_     | 5     |
| falta el estado \_    | 6     |



 

### <a name="automagic-hints-constants"></a>Constantes de sugerencias de automagic



| Constante                               | Value   |
|----------------------------------------|---------|
| sugerencia de VDS \_ \_ MOSTLYREADS                 | 0x0002L |
| sugerencia de VDS \_ \_ OPTIMIZEFORSEQUENTIALREADS  | 0x0004L |
| sugerencia de VDS \_ \_ OPTIMIZEFORSEQUENTIALWRITES | 0x0008L |
| sugerencia de VDS \_ \_ REMAPENABLED                | 0x0020L |
| sugerencia de VDS \_ \_ WRITETHROUGHCACHINGENABLED  | 0x0040L |
| sugerencia de VDS \_ \_ HARDWARECHECKSUMENABLED     | 0x0080L |
| sugerencia de VDS \_ \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Constantes misceláneas



| Constante                     | Value      |
|------------------------------|------------|
| \_ \_ prioridad mínima de regeneración de VDS \_  | 0x0001L    |
| \_información del \_ LUN de VDS de ver \_   | 1          |
| longitud máxima de \_ ComputerName \_    | 15         |
| longitud máxima del \_ PROVIDERNAME \_    | 200        |
| longitud máxima de \_ VERSIONSTRING \_   | 16         |
| \_prop. letra de unidad \_          | N/D        |
| tamaño máximo del \_ nombre de FS \_ \_          | 8          |
| \_IDX de miembro no válido \_         | 0xFFFFFFFF |
| \_longitud de \_ nombre de partición GPT \_ | 36         |
| \_ruta de acceso máxima                    | 260        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de VDS](vds-reference.md)
</dt> </dl>

 

 
