---
description: Cuando se usan las infraestructuras de gráficos del mismo nivel o de agrupación del mismo nivel, la información (registros) que empareja la publicación en un gráfico o grupo se almacena como una base de datos en cada equipo del mismo nivel.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importación y exportación de bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002002"
---
# <a name="database-import-and-export"></a>Importación y exportación de bases de datos

Cuando se usan las infraestructuras de gráficos del mismo nivel o de agrupación del mismo nivel, la información (registros) que empareja la publicación en un gráfico o grupo se almacena como una base de datos en cada equipo del mismo nivel. Para migrar una aplicación de un equipo a otro, puede exportar una base de datos del mismo nivel o de agrupación del mismo nivel desde un equipo y, a continuación, importarla a otro.

La lista siguiente identifica información importante sobre cómo trabajar con bases de datos de:

-   Solo puede importar una base de datos que tenga el mismo gráfico y el mismo identificador del mismo nivel.
-   No se puede llamar a las funciones de importación y exportación si se ha llamado a [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) .

La **infraestructura de gráficos del mismo nivel** usa las siguientes llamadas para importar y exportar una base de datos de registros:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

La **infraestructura de agrupación del mismo nivel** usa las siguientes llamadas para importar y exportar una base de datos de registros:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



