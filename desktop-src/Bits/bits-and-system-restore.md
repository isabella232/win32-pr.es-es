---
title: BITS y Restaurar sistema
description: No todas las versiones de BITS usan el mismo formato para almacenar trabajos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702105"
---
# <a name="bits-and-system-restore"></a>BITS y Restaurar sistema

No todas las versiones de BITS usan el mismo formato para almacenar trabajos. Si devuelve el equipo a un punto de restauración antes de una actualización de BITS, es posible que la versión anterior de BITS no pueda leer la información del trabajo actual. Si esto ocurre, BITS eliminará la lista de trabajos y creará una nueva lista de trabajos vacía. Como resultado, los archivos temporales asociados a la lista de trabajos anteriores no se limpian; para reclamar el espacio en disco, debe eliminar los archivos manualmente.

Los usuarios familiarizados con Windows línea de comandos pueden evitar este problema mediante la herramienta [BITSAdmin](bitsadmin-tool.md) para borrar la lista de trabajos de BITS antes de ejecutar Restaurar sistema. Para borrar la lista de trabajos de BITS, ejecute el siguiente comando:

**bitsadmin /reset /allusers**

Tenga en cuenta que debe tener privilegios de administrador para ejecutar este comando.

 

 




