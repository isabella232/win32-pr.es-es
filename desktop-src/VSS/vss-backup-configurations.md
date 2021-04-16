---
description: Hay una serie de tipos de copia de seguridad admitidos por Convención&\# 8212; incremental, diferencial y completo&\# 8212; compatible con VSS, así como una configuración de copia de seguridad con respecto a VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configuraciones de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696471"
---
# <a name="vss-backup-configurations"></a>Configuraciones de copia de seguridad de VSS

Hay una serie de tipos de copia de seguridad admitidos por Convención (incremental, diferencial y completo) que VSS es consciente de, así como una configuración de copia de seguridad que se da a VSS.

Al definir una configuración de copia de seguridad, un solicitante y los escritores de un sistema indican cómo se escribirán los datos en un dispositivo de almacenamiento, cómo se implementará el mecanismo de instantáneas y qué información se debe guardar. La interacción entre escritores y solicitantes viene determinada por el tipo de copia de seguridad que un solicitante desea realizar y por los tipos (o esquemas) que admite cada escritor:

-   [Estado de copia de seguridad de VSS](vss-backup-state.md)
-   [Compatibilidad con el esquema de copia de seguridad del escritor](writer-backup-schema-support.md)
-   [Compatibilidad con esquemas de nivel de archivo](file-level-schema-support.md)

 

 



