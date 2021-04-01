---
description: La mayoría de las operaciones GET y set solo se ocupan de un componente de la información. La función phoneGetStatus devuelve información de estado completa sobre un dispositivo telefónico a una aplicación.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Estado (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909617"
---
# <a name="status-telephony-api"></a>Estado (API de telefonía)

La mayoría de las operaciones GET y set solo se ocupan de un componente de la información. La función [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) devuelve información de estado completa sobre un dispositivo telefónico a una aplicación.

Como se mencionó anteriormente, cada vez que un elemento de estado cambia en el dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la función de aplicación. Los parámetros de este mensaje incluyen un identificador del dispositivo telefónico y una indicación del elemento de estado que ha cambiado.

Una aplicación puede utilizar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para seleccionar los cambios de estado específicos para los que desea recibir notificaciones. En consecuencia, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) devuelve los cambios de estado para los que la aplicación desea recibir notificaciones.

 

 



