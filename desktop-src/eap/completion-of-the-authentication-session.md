---
title: Finalización de la sesión de autenticación
description: Una vez completada la sesión de autenticación, el servicio de autenticación llama a la función RasEapEnd para permitir que el protocolo de autenticación desasigne su búfer de trabajo.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948475"
---
# <a name="completion-of-the-authentication-session"></a>Finalización de la sesión de autenticación

Una vez completada la sesión de autenticación, el servicio de autenticación llama a la función [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) para permitir que el protocolo de autenticación desasigne su búfer de trabajo. Esta acción se realiza independientemente de si la autenticación se ha realizado correctamente. Llamar a **la función RasEapEnd** garantiza que no se realizan más llamadas al protocolo de autenticación mediante ese usuario o contexto concretos sin llamar primero a [**RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))

 

 