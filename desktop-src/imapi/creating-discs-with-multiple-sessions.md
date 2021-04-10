---
title: Crear discos con varias sesiones
description: IMAPi es capaz de crear discos de datos de varias sesiones. Hay algunas consideraciones que se deben tener en cuenta al crear un disco de varias sesiones.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268615"
---
# <a name="creating-discs-with-multiple-sessions"></a>Crear discos con varias sesiones

IMAPi es capaz de crear discos de datos de varias sesiones. Hay algunas consideraciones que se deben tener en cuenta al crear un disco de varias sesiones.

El método [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina si hay un disco de varias sesiones de IMAPI en la unidad activa al establecer. Si es así, IMAPi entra en modo de sesión múltiple automáticamente. El uso de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) después de que se haya establecido el modo de varias sesiones hace que IMAPI vuelva al modo de sesión única. Esto significa que se requiere un disco en blanco para una grabación de [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) . Si el disco está en modo de varias sesiones, el mismo disco debe estar en la grabadora activa o se devolverá un código de error de IMAPi \_ E \_ WRONGDISC.

La selección de una grabadora en formato Joliet hace que IMAPi Lea información del disco instalado actualmente. Si el disco es un disco Joliet de IMAPi anterior que tiene espacio para otra sesión, IMAPi se establece automáticamente en modo de varias sesiones. Este disco debe estar presente en la grabadora activa al llamar a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

Cerrar la primera sesión en un disco requiere 21 MB. Cada sesión adicional requiere 11 MB para cerrarse.

 

 




