---
title: Funciones de programación
description: Las funciones de servicio de programación de administración de red envían y administran trabajos que se ejecutan en un equipo especificado en un momento determinado (o veces) en el futuro.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676469"
---
# <a name="schedule-functions"></a>Funciones de programación

Las funciones de servicio de programación de administración de red envían y administran trabajos que se ejecutan en un equipo especificado en un momento determinado (o veces) en el futuro. Los trabajos pueden incluir comandos y programas. Las funciones administran los trabajos en equipos remotos y locales, siempre que el servicio de programación se esté ejecutando en el equipo.

A continuación se enumeran las funciones de servicio de programación.



| Función                                                                     | Descripción                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Envía un trabajo para que se ejecute en una fecha y hora futuras especificadas.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Cancela un intervalo de trabajos en cola para ejecutarse en un equipo.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Enumera los trabajos en cola en un equipo especificado.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Devuelve información acerca de un trabajo determinado en cola en un equipo. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera el nombre de la cuenta de servicio de AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Establece el nombre y la contraseña de la cuenta de servicio en.                   |



 

Para que las funciones de programación de administración de redes se realicen correctamente, el autor de la llamada debe tener privilegios de administrador en el equipo en el que se ejecuta el servicio de programación. Las funciones de servicio de programación también se conocen como funciones "Job" y "AT Command". Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

La función [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) utiliza la estructura [**at \_ info**](/windows/desktop/api/Lmat/ns-lmat-at_info) para especificar información al enviar un trabajo y la función [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) para recuperar información sobre un trabajo que se ha enviado. [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) utiliza la estructura [**at \_ enum**](/windows/desktop/api/Lmat/ns-lmat-at_enum) para enumerar y devolver información sobre toda una cola de trabajos enviados.

 

 