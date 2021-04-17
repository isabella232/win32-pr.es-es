---
description: El seguimiento de CallHub es una nueva característica de la versión 3,0 de TAPI.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Compatibilidad con CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678119"
---
# <a name="callhub-support"></a>Compatibilidad con CallHub

El seguimiento de CallHub es una nueva característica de la versión 3,0 de TAPI. La funcionalidad de CallHub se agregó a los elementos de programación de TAPI 2,1 con la entrega de Windows 2000. Un *CallHub* representa una vista de terceros de una llamada, y los identificadores de llamada de TAPI representan la vista de la primera parte de una llamada. Con el seguimiento de CallHub, se solicita al proveedor de servicios que siga CallHubs y proporcione información acerca de la llamada durante la vigencia de una CallHub. A medida que las entidades nuevas se unen y salen del CallHub, el proveedor de servicios debe informar a TAPI.

No es necesario que un proveedor de servicios implemente nuevas funciones para admitir CallHub. Simplemente tiene que rellenar el miembro **dwCallID** de la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) . En TAPI 3, TAPI recopila todas las llamadas con el mismo **dwCallID** y crea un identificador de CallHub que la aplicación puede usar para realizar el seguimiento de la llamada.

 

 
