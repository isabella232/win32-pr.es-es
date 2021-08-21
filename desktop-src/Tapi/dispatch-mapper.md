---
description: El asignador de distribución se crea mediante COM CoCreateInstance y expone una interfaz, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Asignador de distribución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0880228ab608abe5f599d58bb47d211d1458dd49636a9bdc992f31dfa26c028
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866689"
---
# <a name="dispatch-mapper"></a>Asignador de distribución

El asignador de distribución se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITDispatchMapper.**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper) Esta interfaz permite a una aplicación recuperar el puntero de envío de otra interfaz en un objeto , dado el puntero de envío de una interfaz y el GUID de otra. Esta interfaz se proporciona para ayudar a los programadores a usar aplicaciones de scripting que no proporcionan un medio para sondear fácilmente las interfaces de un objeto.

El Asignador de distribución usa la interfaz **IObjectSafety** de un objeto para asegurarse de que el objeto es seguro para el scripting en la interfaz solicitada. Si el objeto no implementa **IObjectSafety** o si el objeto no es seguro en esta interfaz determinada, se producirá un error en la llamada.

 

 



