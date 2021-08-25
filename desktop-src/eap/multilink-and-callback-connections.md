---
title: Conexiones multivinculación y devolución de llamada
description: Para el primer vínculo de una conexión de varios vínculos, el servicio de autenticación establece la marca RAS EAP FLAG FIRST LINK en el miembro fFlags de la \_ \_ estructura PPP EAP \_ \_ \_ \_ INPUT.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852325"
---
# <a name="multilink-and-callback-connections"></a>Conexiones multivinculación y devolución de llamada

Para el primer vínculo de una conexión de varios vínculos, el servicio de autenticación establece la marca RAS EAP FLAG FIRST LINK en el miembro \_ \_ \_ \_ **fFlags** [**\_ \_**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) de la estructura PPP EAP INPUT. El protocolo de autenticación puede usar la presencia de esta marca para determinar si se debe presentar una interfaz de usuario específicamente para el primer vínculo de una conexión de varios vínculos.

Si la conexión está configurada para que el servidor vuelva a llamar al equipo cliente, la marca RAS EAP FLAG FIRST LINK no se establecerá \_ \_ en la \_ \_ devolución de llamada.

Si el protocolo de autenticación establece el miembro **fSaveConnectionData** de [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en **TRUE,** los vínculos posteriores de la conexión de varios vínculos reciben los nuevos datos específicos de la conexión. Sin embargo, en el caso de los datos específicos del usuario, el protocolo de autenticación sigue teniendo los datos originales específicos del usuario incluso si establece el miembro **fSaveUserData** de **PPP EAP \_ \_ OUTPUT** en **TRUE.**

El protocolo de autenticación puede usar [una interfaz de usuario interactiva para](interactive-user-interface.md) recopilar datos para un vínculo determinado de una conexión de varios vínculos. En este caso, el servicio de autenticación pone los datos resultantes a disposición del protocolo de autenticación durante los vínculos posteriores. Sin embargo, estos datos nunca se guardan en el almacenamiento persistente.

 

 




