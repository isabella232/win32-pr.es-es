---
description: Cuando se usa el grafo del mismo nivel o las infraestructuras de agrupación del mismo nivel, la información (registros) que publican en un grafo o grupo se almacena como una base de datos en cada equipo del mismo nivel.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importación y exportación de bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc047e6f58c7aeab07f6d13f8f7364f3f2f1191e50320513bc153e34c4c042c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979065"
---
# <a name="database-import-and-export"></a>Importación y exportación de bases de datos

Cuando se usa el grafo del mismo nivel o las infraestructuras de agrupación del mismo nivel, la información (registros) que publican en un grafo o grupo se almacena como una base de datos en cada equipo del mismo nivel. Para migrar una aplicación de un equipo a otro, puede exportar una base de datos de grafos del mismo nivel o agrupación del mismo nivel desde un equipo y, a continuación, importarla a otro.

En la lista siguiente se identifica información importante sobre cómo trabajar con bases de datos:

-   Solo puede importar una base de datos que tenga el mismo gráfico y el mismo identificador del mismo nivel.
-   No se puede llamar a las funciones de importación y exportación si se ha llamado a [**PeerGraphListen,**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)o [**PeerGraphConnect.**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)

**Peer Graphing Infrastructure usa** las siguientes llamadas para importar y exportar una base de datos de registros:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

**La infraestructura de agrupación del mismo** nivel usa las siguientes llamadas para importar y exportar una base de datos de registros:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



