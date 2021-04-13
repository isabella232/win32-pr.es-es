---
title: Finalización de la sesión de autenticación
description: Una vez completada la sesión de autenticación, el servicio de autenticación llama a la función RasEapEnd para permitir que el protocolo de autenticación Desasigne su búfer de trabajo.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420604"
---
# <a name="completion-of-the-authentication-session"></a>Finalización de la sesión de autenticación

Una vez completada la sesión de autenticación, el servicio de autenticación llama a la función [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) para permitir que el protocolo de autenticación Desasigne su búfer de trabajo. Esta acción se lleva a cabo independientemente de si la autenticación se realizó correctamente. La llamada a la función **RasEapEnd** garantiza que no se realizan más llamadas al Protocolo de autenticación con ese usuario o contexto concretos sin llamar primero a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 