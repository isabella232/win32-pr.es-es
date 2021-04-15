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
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="141b4-103">Conexiones de devolución de llamada y multivínculo</span><span class="sxs-lookup"><span data-stu-id="141b4-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="141b4-104">Para el primer vínculo en una conexión de multivínculo, el servicio de autenticación establece la \_ \_ marca de enlace EAP de Ras \_ primero \_ en el miembro **fFlags** de la estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) .</span><span class="sxs-lookup"><span data-stu-id="141b4-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="141b4-105">El protocolo de autenticación puede usar la presencia de esta marca para determinar si se debe presentar una interfaz de usuario específica para el primer vínculo de una conexión de multivínculo.</span><span class="sxs-lookup"><span data-stu-id="141b4-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="141b4-106">Si la conexión está configurada para que el servidor vuelva a llamar al equipo cliente, la \_ \_ marca de \_ vínculo de marca EAP de Ras \_ no se establecerá en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="141b4-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="141b4-107">Si el protocolo de autenticación establece el miembro **fSaveConnectionData** de la [**salida de PPP \_ \_ EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en **true**, los vínculos posteriores de la conexión de multivínculo reciben los nuevos datos específicos de la conexión.</span><span class="sxs-lookup"><span data-stu-id="141b4-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="141b4-108">Sin embargo, en el caso de los datos específicos del usuario, el protocolo de autenticación continúa con los datos originales específicos del usuario, incluso si establece el miembro **fSaveUserData** de la **salida de PPP \_ \_ EAP** en **true**.</span><span class="sxs-lookup"><span data-stu-id="141b4-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="141b4-109">El protocolo de autenticación puede usar una [interfaz de usuario interactiva](interactive-user-interface.md) para recopilar datos de un vínculo determinado de una conexión de vínculos múltiples.</span><span class="sxs-lookup"><span data-stu-id="141b4-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="141b4-110">En este caso, el servicio de autenticación hace que los datos resultantes estén disponibles para el protocolo de autenticación durante los vínculos posteriores.</span><span class="sxs-lookup"><span data-stu-id="141b4-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="141b4-111">Sin embargo, estos datos nunca se guardan en un almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="141b4-111">However, this data is never saved to persistent storage.</span></span>

 

 




