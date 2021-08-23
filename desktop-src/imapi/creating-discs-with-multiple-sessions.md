---
title: Creación de discos con varias sesiones
description: IMAPI es capaz de crear discos de datos de varias sesiones. Hay algunas consideraciones que debe tener en cuenta al crear un disco de varias sesiones.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b108a6b7b07d6d82230362899da26e7264e62a460c197338e223f0e95078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977125"
---
# <a name="creating-discs-with-multiple-sessions"></a>Creación de discos con varias sesiones

IMAPI es capaz de crear discos de datos de varias sesiones. Hay algunas consideraciones que debe tener en cuenta al crear un disco de varias sesiones.

El [**método IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina si hay un disco de sesión múltiple IMAPI en la unidad activa tras la configuración. Si es así, IMAPI entra automáticamente en modo de sesión múltiple. El [**uso de ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) una vez establecido el modo de sesión múltiple hace que IMAPI vuelva al modo de sesión única. Esto significa que se requiere un disco en blanco para una [**grabación de RecordDisc.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) Si el disco está en modo de sesión múltiple, el mismo disco debe estar en la grabadora activa o se devolverá un código de error de IMAPI \_ E \_ WRONGDISC.

La selección de una grabadora en formato Joliet hace que IMAPI lea información del disco instalado actualmente. Si el disco es un disco imapi joliet anterior que tiene espacio para otra sesión, IMAPI se establece automáticamente en modo de varias sesiones. Este disco debe estar presente en la grabadora activa al llamar a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

El cierre de la primera sesión en un disco requiere 21 MB. Cada sesión adicional requiere 11 MB para cerrarse.

 

 




