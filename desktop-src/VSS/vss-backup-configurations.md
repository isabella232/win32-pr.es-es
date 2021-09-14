---
description: Hay una serie de tipos de copia de seguridad admitidos convencionalmente&\# 8212; incremental, diferencial y&completo 8212; que VSS conoce, así como una configuración de copia de seguridad \# en VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configuraciones de copia de seguridad de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068546"
---
# <a name="vss-backup-configurations"></a>Configuraciones de copia de seguridad de VSS

Hay una serie de tipos de copia de seguridad admitidos convencionalmente (incremental, diferencial y completo) que VSS conoce, así como una configuración de copia de seguridad en VSS.

Al definir una configuración de copia de seguridad, un solicitante y los escritores de un sistema indican cómo se escribirán los datos en un dispositivo de almacenamiento, cómo se implementará el mecanismo de instantáneas y qué información debe guardarse. La interacción entre escritores y solicitantes viene determinada por el tipo de copia de seguridad que un solicitante quiere realizar y los tipos (o esquemas) que cada escritor puede admitir:

-   [Estado de copia de seguridad de VSS](vss-backup-state.md)
-   [Compatibilidad con esquemas de copia de seguridad del escritor](writer-backup-schema-support.md)
-   [Compatibilidad con esquemas de nivel de archivo](file-level-schema-support.md)

 

 



