---
description: TAPI 3 define cinco objetos principales de ACD que el controlador del agente pone en cola el grupo ACD del agente y la sesión del agente. También extiende el objeto TAPI con una interfaz adicional ITTAPICallCenter.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: Acerca de los controles del centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0ac7774d2a1ee1b4be45714898461615eb724603ce9f8d249b815046d8d7bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949491"
---
# <a name="about-call-center-controls"></a>Acerca de los controles del centro de llamadas

TAPI 3 define cinco objetos principales de ACD: el controlador del agente, la cola, el grupo de ACD, el agente y la sesión del agente. También extiende el objeto TAPI con una interfaz adicional: [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Agent (Objeto)

El objeto Agent representa un agente capaz de controlar las llamadas. Normalmente se trata de una persona, pero puede ser un IVR o alguna otra combinación de software y hardware. Los agentes son clave para un centro de llamadas. son responsables de recibir y procesar llamadas entrantes y, en ocasiones, realizar llamadas salientes a clientes o clientes potenciales.

En TAPI, el objeto Agente se relaciona directamente con una cuenta de usuario, para proporcionar compatibilidad con los sistemas de conmutación heredados existentes. Además, para proporcionar compatibilidad con sistemas de conmutación heredados existentes, el Agente también puede estar relacionado con un identificador de agente de conmutador.

El objeto Agent expone la [**interfaz ITAgent.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) Esta interfaz implementa métodos que pueden crear una sesión del Agente y recuperar estadísticas como el número total de llamadas que se controlan. Las aplicaciones pueden usar el objeto Agente para manipular el estado del agente y determinar las estadísticas globales del agente.

## <a name="agent-handler-object"></a>Objeto de controlador de agente

Un controlador de agente representa software o hardware capaz de pasar llamadas a un grupo de agentes. Normalmente, se trata de un conmutador propietario que conecta líneas externas a teléfonos en las estaciones de agente. La mayoría de los sistemas ACD solo tienen un conmutador de este tipo, pero las operaciones grandes pueden tener más. En el caso de que un agente tenga dispositivos en más de un sistema ACD, el agente verá un número correspondiente de objetos de controlador de agente. También habrá una instancia del objeto agente relacionada con la apariencia del agente en cada sistema ACD.

El objeto Controlador del agente expone la [**interfaz ITAgentHandler.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) Esta interfaz implementa métodos que proporcionan información sobre los grupos [de ACD](#acd-group-object) asociados al controlador del agente y las direcciones que puede usar.

## <a name="agent-session-object"></a>Objeto de sesión del Agente

Una sesión del agente representa a un agente que ha iniciado sesión y está calificado para controlar las llamadas de un grupo [de ACD determinado.](#acd-group-object) Una sesión del agente es un objeto creado dinámicamente, que relaciona un agente con un grupo de ACD, para el que proporcionará el servicio, y también con la dirección, donde recibirá llamadas (asistencia, estación, teléfono, etc.). Las aplicaciones pueden usar el objeto Sesión del agente para realizar un seguimiento de la actividad del agente dentro de un grupo de ACD determinado.

El objeto Agent Session expone la [**interfaz ITAgentSession.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) Esta interfaz implementa métodos que pueden recuperar información como el tiempo medio de conversación de una llamada.

## <a name="acd-group-object"></a>Objeto de grupo ACD

Un grupo de ACD representa una clase de llamadas que requiere un tipo determinado de control. Por ejemplo, algunas llamadas entrantes para el centro de llamadas de un banco pueden afectar a las cuentas existentes y otras pueden estar relacionadas con cuentas nuevas. Algunos agentes pueden tener experiencia en ambas áreas, pero la mayoría se especializarán en una. Se crearán grupos de ACD para controlar cada tipo de llamada. Un grupo de ACD proporciona una o varias colas. A medida que se clasifican las llamadas entrantes, se pasarán a las colas asociadas al grupo de ACD correspondiente. Una llamada que sale de la cola se [](#agent-session-object) pasa a un agente que ha creado un objeto de sesión del agente que indica que pueden controlar las llamadas desde ese grupo de ACD.

El objeto de grupo ACD expone la [**interfaz ITACDGroup.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) Esta interfaz implementa métodos que proporcionan acceso a las colas asociadas al grupo de ACD actual.

## <a name="queue-object"></a>Objeto Queue

El objeto Queue representa un punto dentro del sistema ACD donde las llamadas se mantienen temporalmente pendientes. El objeto Queue expone la [**interfaz ITQueue.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) Esta interfaz implementa métodos que recopilan estadísticas en una cola, como el número de llamadas actualmente en cola. El [proxy de ACD](acd-proxy.md) usa esta información para distribuir las llamadas a los agentes y generar informes administrativos.

El acceso a un objeto Queue permite a una aplicación leer diversas estadísticas estándar relacionadas con el uso de la cola, pero no le ofrece la capacidad de controlar las llamadas en la cola. Solo las aplicaciones con acceso a las direcciones y líneas asociadas (normalmente la aplicación proxy de ACD) podrían controlar las llamadas en la cola.

La mayoría de las colas se relacionan directamente con un objeto de [grupo de ACD](#acd-group-object)y contendrán una llamada hasta que un agente pueda controlarlo. Pueden existir otras colas para permitir guías de llamadas complejas (la ruta de acceso definida que una llamada sin respuesta tomará a través de un modificador). Por ejemplo, las llamadas se pueden colocar en colas de retención antes de enrutar a una cola a la que atiende un grupo de ACD.

 

 
