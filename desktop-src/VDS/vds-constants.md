---
description: Constantes VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9fa0c6196e1085de3a5433750b890e2ad3bc42f4a86022587f02157521eacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125698"
---
# <a name="vds-constants"></a>Constantes VDS

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Las constantes VDS se clasifican de la siguiente manera:

-   [Constantes de estado de objeto](#object-status-constants)
-   [Constantes de sugerencias de Automagic](#automagic-hints-constants)
-   [Constantes misceláneas](#miscellaneous-constants)

### <a name="object-status-constants"></a>Constantes de estado de objeto



| Constante           | Valor |
|--------------------|-------|
| ESTADO \_ DESCONOCIDO    | 0     |
| ESTADO \_ EN LÍNEA     | 1     |
| ESTADO \_ NO \_ LISTO | 2     |
| ESTADO \_ SIN \_ MEDIOS  | 3     |
| ESTADO SIN \_ CONEXIÓN    | 4     |
| ERROR DE \_ ESTADO     | 5     |
| ESTADO \_ QUE FALTA    | 6     |



 

### <a name="automagic-hints-constants"></a>Constantes de sugerencias de Automagic



| Constante                               | Value   |
|----------------------------------------|---------|
| SUGERENCIAS \_ VDS \_ PRINCIPALMENTEREADS                 | 0x0002L |
| OPTIMIZACIÓN \_ DE SUGERENCIAS \_ VDSFORSEQUENTIALREADS  | 0x0004L |
| OPTIMIZACIÓN \_ DE SUGERENCIAS \_ VDSFORSEQUENTIALWRITES | 0x0008L |
| SUGERENCIA VDS \_ \_ REMAPENABLED                | 0x0020L |
| \_WRITETHROUGHCACHINGENABLED DE \_ SUGERENCIAS VDS  | 0x0040L |
| \_ \_ HARDWARECHECKSUMENABLED DE SUGERENCIA VDS     | 0x0080L |
| SUGERENCIA VDS \_ \_ ISYANKABLE                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Constantes misceláneas



| Constante                     | Valor      |
|------------------------------|------------|
| VDS \_ REBUILD \_ PRIORITY \_ MIN  | 0x0001L    |
| INFORMACIÓN DE LUN DE VER \_ VDS \_ \_   | 1          |
| LONGITUD \_ MÁXIMA DE \_ NOMBREDEEQUIPO    | 15         |
| LONGITUD \_ MÁXIMA DE \_ PROVIDERNAME    | 200        |
| LONGITUD \_ MÁXIMA DE VERSIONSTRING \_   | 16         |
| PROP \_ DE LETRA DE \_ UNIDAD          | N/D        |
| MAX \_ FS \_ NAME \_ SIZE          | 8          |
| IDX \_ DE \_ MIEMBRO NO VÁLIDO         | 0xFFFFFFFF |
| LONGITUD DEL NOMBRE \_ DE PARTICIÓN \_ DE GPT \_ | 36         |
| RUTA DE \_ ACCESO MÁXIMA                    | 260        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de VDS](vds-reference.md)
</dt> </dl>

 

 
