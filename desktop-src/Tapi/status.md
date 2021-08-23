---
description: La mayoría de las operaciones get y set se tratan solo con un componente de información. La función phoneGetStatus devuelve información de estado completa sobre un dispositivo de teléfono a una aplicación.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Estado (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fd9191d4b1808ca2dc5ff20ce509b58ad27a78a354aeca4ca83f8aa60dafa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861832"
---
# <a name="status-telephony-api"></a>Estado (API de telefonía)

La mayoría de las operaciones get y set se tratan solo con un componente de información. La [**función phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) devuelve información de estado completa sobre un dispositivo de teléfono a una aplicación.

Como se mencionó anteriormente, cada vez que cambia un elemento de estado en el dispositivo telefónico, se envía un mensaje [**PHONE \_ STATE**](phone-state.md) a la función de aplicación. Los parámetros de este mensaje incluyen un identificador para el dispositivo de teléfono y una indicación del elemento de estado que ha cambiado.

Una aplicación puede usar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para seleccionar los cambios de estado específicos para los que desea recibir una notificación. En consecuencia, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) devuelve los cambios de estado para los que se quiere notificar a la aplicación.

 

 



