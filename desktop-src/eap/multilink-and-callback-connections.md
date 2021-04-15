---
title: Conexiones de devolución de llamada y multivínculo
description: Para el primer vínculo en una conexión de multivínculo, el servicio de autenticación establece la \_ \_ marca de enlace EAP de Ras \_ primero \_ en el miembro fFlags de la \_ estructura de entrada EAP de PPP \_ .
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105714315"
---
# <a name="multilink-and-callback-connections"></a>Conexiones de devolución de llamada y multivínculo

Para el primer vínculo en una conexión de multivínculo, el servicio de autenticación establece la \_ \_ marca de enlace EAP de Ras \_ primero \_ en el miembro **fFlags** de la estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . El protocolo de autenticación puede usar la presencia de esta marca para determinar si se debe presentar una interfaz de usuario específica para el primer vínculo de una conexión de multivínculo.

Si la conexión está configurada para que el servidor vuelva a llamar al equipo cliente, la \_ \_ marca de \_ vínculo de marca EAP de Ras \_ no se establecerá en la devolución de llamada.

Si el protocolo de autenticación establece el miembro **fSaveConnectionData** de la [**salida de PPP \_ \_ EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en **true**, los vínculos posteriores de la conexión de multivínculo reciben los nuevos datos específicos de la conexión. Sin embargo, en el caso de los datos específicos del usuario, el protocolo de autenticación continúa con los datos originales específicos del usuario, incluso si establece el miembro **fSaveUserData** de la **salida de PPP \_ \_ EAP** en **true**.

El protocolo de autenticación puede usar una [interfaz de usuario interactiva](interactive-user-interface.md) para recopilar datos de un vínculo determinado de una conexión de vínculos múltiples. En este caso, el servicio de autenticación hace que los datos resultantes estén disponibles para el protocolo de autenticación durante los vínculos posteriores. Sin embargo, estos datos nunca se guardan en un almacenamiento persistente.

 

 




