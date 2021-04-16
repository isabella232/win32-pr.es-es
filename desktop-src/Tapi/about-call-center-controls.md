---
description: TAPI 3 define cinco objetos ACD principales que el controlador de agente ha puesto en cola el agente y la sesión del agente. También extiende el objeto TAPI con una interfaz adicional ITTAPICallCenter.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: Acerca de los controles de centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156492"
---
# <a name="about-call-center-controls"></a>Acerca de los controles de centro de llamadas

TAPI 3 define cinco objetos ACD principales: el controlador del agente, la cola, el grupo ACD, el agente y la sesión del agente. También extiende el objeto TAPI con una interfaz adicional: [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Objeto agente

El objeto de agente representa un agente capaz de controlar las llamadas. Normalmente se trata de una persona, pero puede ser un IVR o cualquier otra combinación de software y hardware. Los agentes son clave para un centro de llamadas; son responsables de recibir y procesar las llamadas entrantes y, en ocasiones, realizar llamadas salientes a clientes o clientes potenciales.

En TAPI, el objeto de agente se relaciona directamente con una cuenta de usuario para proporcionar compatibilidad con sistemas de conmutación heredados existentes. Además, para proporcionar compatibilidad con los sistemas de conmutación heredados existentes, el agente también puede estar relacionado con un ID. de agente de conmutador.

El objeto Agent expone la interfaz [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) . Esta interfaz implementa métodos que pueden crear una sesión del agente y recuperar estadísticas como el número total de llamadas administradas. Las aplicaciones pueden usar el objeto de agente para manipular el estado del agente y determinar las estadísticas globales del agente.

## <a name="agent-handler-object"></a>Objeto de controlador de agente

Un controlador de agente representa el software o hardware capaz de pasar llamadas a un grupo de agentes. Normalmente, se trata de un conmutador propietario que se conecta fuera de las líneas a los teléfonos de las estaciones de agente. La mayoría de los sistemas ACD solo tienen un conmutador de este tipo, pero las operaciones grandes pueden tener más. En el caso de que un agente tenga dispositivos en más de un sistema ACD, el agente verá un número correspondiente de objetos de controlador de agente. También habrá una instancia del objeto de agente relacionada con la apariencia del agente en cada sistema ACD.

El objeto de controlador de agente expone la interfaz [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) . Esta interfaz implementa métodos que proporcionan información sobre los [grupos ACD](#acd-group-object) asociados al controlador del agente y las direcciones que puede usar.

## <a name="agent-session-object"></a>Objeto de sesión del agente

Una sesión del agente representa un agente que ha iniciado sesión y está calificado para controlar las llamadas de un [Grupo ACD](#acd-group-object)determinado. Una sesión del agente es un objeto creado dinámicamente que relaciona un agente con un grupo ACD, para el que proporcionará el servicio y también la dirección, donde recibirá llamadas (torreta, estación, teléfono, etc.). Las aplicaciones pueden usar el objeto de sesión del agente para realizar el seguimiento de la actividad del agente en un grupo de ACD determinado.

El objeto de sesión del agente expone la interfaz [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) . Esta interfaz implementa métodos que pueden recuperar información como el tiempo medio de la conversación para una llamada.

## <a name="acd-group-object"></a>Objeto de grupo ACD

Un grupo ACD representa una clase de llamadas que requiere un tipo de control determinado. Por ejemplo, algunas llamadas entrantes del centro de llamadas de un banco pueden afectar a las cuentas existentes y otras pueden estar relacionadas con nuevas cuentas. Algunos agentes pueden tener experiencia en ambas áreas, pero la mayoría se especializará en una. Los grupos ACD se crearán para administrar cada tipo de llamada. Un grupo ACD pone a su servicio una o más colas. A medida que se clasifiquen las llamadas entrantes, se pasarán a las colas asociadas al grupo ACD correspondiente. Una llamada que va fuera de la cola se pasa a un agente que ha creado un [objeto de sesión del agente](#agent-session-object) que indica que pueden administrar las llamadas de ese grupo ACD.

El objeto ACD Group expone la interfaz [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) . Esta interfaz implementa métodos que proporcionan acceso a las colas asociadas al grupo ACD actual.

## <a name="queue-object"></a>Queue (objeto)

El objeto Queue representa un punto dentro del sistema ACD en el que las llamadas se mantienen temporalmente como acciones pendientes. El objeto Queue expone la interfaz [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) . Esta interfaz implementa métodos que recopilan estadísticas de una cola, como el número de llamadas actualmente en cola. El [proxy ACD](acd-proxy.md) usa esta información para distribuir las llamadas a los agentes y para generar informes administrativos.

El acceso a un objeto de cola permite a una aplicación leer diversas estadísticas estándar relacionadas con el uso de la cola, pero no ofrece la posibilidad de controlar las llamadas en la cola. Solo las aplicaciones con acceso a las direcciones y líneas asociadas (normalmente la aplicación de proxy ACD) podrán controlar las llamadas en la cola.

La mayoría de las colas se relacionan directamente con un [objeto de grupo ACD](#acd-group-object)y contendrán una llamada hasta que un agente pueda controlarla. Pueden existir otras colas para permitir guías de llamadas complejas (la ruta de acceso definida que una llamada no responde pasará a través de un modificador). Por ejemplo, las llamadas se pueden colocar en la retención de colas antes de enrutarse a una cola a la que presta servicio un grupo ACD.

 

 
