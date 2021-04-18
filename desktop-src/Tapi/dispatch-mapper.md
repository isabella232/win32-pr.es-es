---
description: El asignador de envío se crea mediante COM CoCreateInstance y expone una interfaz, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Asignador de envío
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687514"
---
# <a name="dispatch-mapper"></a>Asignador de envío

El asignador de envío se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper). Esta interfaz permite a una aplicación recuperar el puntero de envío de otra interfaz en un objeto, dado el puntero de envío de una interfaz y el GUID de otro. Esta interfaz se proporciona para ayudar a los programadores a usar aplicaciones de scripting que no proporcionan un medio para sondear fácilmente las interfaces en un objeto.

El asignador de envío utiliza la interfaz **IObjectSafety** del objeto para asegurarse de que el objeto es seguro para el scripting en la interfaz solicitada. Si el objeto no implementa **IObjectSafety**, o si el objeto no es seguro en esta interfaz determinada, se producirá un error en la llamada.

 

 



