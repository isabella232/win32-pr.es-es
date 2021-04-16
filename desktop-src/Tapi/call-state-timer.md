---
description: Actualmente, todo el tiempo de llamadas se deja en las aplicaciones.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Temporizador de estado de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677451"
---
# <a name="call-state-timer"></a>Temporizador de estado de llamada

Actualmente, todo el tiempo de llamadas se deja en las aplicaciones. Esto puede ser oneroso si la aplicación está supervisando un gran número de llamadas y, si hay varias aplicaciones presentes, posiblemente en varios servidores, puede ser necesario para todo el mantenimiento de los temporizadores en las mismas llamadas. Por lo tanto, tiene más sentido que el servidor controle la sincronización del estado de la llamada.

El miembro **tStateEntryTime** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permite el control de tiempo de las llamadas en los Estados en los que se va a informar. El miembro (de tipo **SYSTIME**) indica la hora a la que se escribió el estado actual.

 

 



