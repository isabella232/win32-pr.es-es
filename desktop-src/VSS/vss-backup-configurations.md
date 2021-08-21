---
description: Hay una serie de tipos de copia de seguridad compatibles convencionalmente&\# 8212;incremental, diferencial y&8212; que VSS conoce, así como una configuración de copia de seguridad \# en VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configuraciones de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8552bc379be4fc2bf7301043355a1a4417a59154ea15c36061b9cfd13c5d209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056343"
---
# <a name="vss-backup-configurations"></a>Configuraciones de copia de seguridad de VSS

Hay una serie de tipos de copia de seguridad admitidos convencionalmente (incremental, diferencial y completo) que VSS conoce, así como una configuración de copia de seguridad en VSS.

Al definir una configuración de copia de seguridad, un solicitante y los escritores de un sistema indican cómo se escribirán los datos en un dispositivo de almacenamiento, cómo se implementará el mecanismo de instantáneas y qué información debe guardarse. La interacción entre escritores y solicitantes viene determinada por el tipo de copia de seguridad que un solicitante quiere realizar y los tipos (o esquemas) que cada escritor puede admitir:

-   [Estado de copia de seguridad de VSS](vss-backup-state.md)
-   [Compatibilidad con esquemas de copia de seguridad de escritores](writer-backup-schema-support.md)
-   [Compatibilidad con esquemas de nivel de archivo](file-level-schema-support.md)

 

 



