---
title: BITS y restauración del sistema
description: No todas las versiones de BITS usan el mismo formato para almacenar los trabajos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075262"
---
# <a name="bits-and-system-restore"></a>BITS y restauración del sistema

No todas las versiones de BITS usan el mismo formato para almacenar los trabajos. Si devuelve el equipo a un punto de restauración antes de una actualización de BITS, es posible que la versión anterior de BITS no pueda leer la información del trabajo actual. Si esto ocurre, BITS eliminará la lista de trabajos y creará una nueva lista de trabajos vacía. Como resultado, los archivos temporales asociados a la lista de trabajos anteriores no se limpian; para recuperar el espacio en disco, debe eliminar manualmente los archivos.

Los usuarios familiarizados con la línea de comandos de Windows pueden evitar este problema mediante la [herramienta BITSAdmin](bitsadmin-tool.md) para borrar la lista de trabajos de bits antes de ejecutar Restaurar sistema. Para borrar la lista de trabajos de BITS, ejecute el siguiente comando:

**bitsadmin/RESET/AllUsers**

Tenga en cuenta que debe tener privilegios de administrador para ejecutar este comando.

 

 




