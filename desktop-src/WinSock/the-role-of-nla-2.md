---
description: El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que podrían moverse entre redes diferentes y para seleccionar configuraciones óptimas cuando hay más de uno disponible.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: El rol de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733345"
---
# <a name="the-role-of-nla"></a>El rol de NLA

El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que podrían moverse entre redes diferentes y para seleccionar configuraciones óptimas cuando hay más de uno disponible. Por ejemplo, un equipo inalámbrico itinerante entre redes físicas puede usar NLA para determinar la configuración adecuada en función de la información sobre su conexión de red disponible. NLA también resulta valioso cuando un equipo de varias propiedades tiene una conexión física a una red, mientras que también está conectado a otra a través de una conexión de acceso telefónico o un túnel.

En el pasado, los desarrolladores tenían que obtener información sobre una interfaz de red lógica y, por tanto, tomar decisiones sobre la conectividad de red, en función de una gran cantidad de información de red dispare. En esas circunstancias, los desarrolladores tenían que elegir la interfaz de red adecuada en función de la dirección IP, la subred de la interfaz, el nombre del sistema de nombres de dominio (DNS) asociado a la interfaz, la dirección MAC de una NIC, un nombre de red inalámbrica u otra información de red. NLA mitiga este problema proporcionando una interfaz estándar para enumerar la información de datos adjuntos de red lógica, correlacionarla con la información de la interfaz de red física y, a continuación, proporcionar una notificación cuando se invalida la información devuelta anteriormente.

NLA proporciona la siguiente información de ubicación de red:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identidad de red lógica
</dt> <dd>

NLA intenta primero identificar una red lógica por su nombre de dominio DNS. Si una red lógica no tiene un nombre de dominio, NLA identifica la red a partir de la información estática personalizada almacenada en el Registro y, por último, desde su dirección de subred.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces de red lógicas
</dt> <dd>

Para cada red a la que está conectado un equipo, NLA proporciona un *AdapterName* que identifica de forma única una interfaz física como una NIC o una interfaz lógica como una conexión RAS. A continuación, AdapterName se puede usar con funciones disponibles en la API del asistente de IP para obtener características de interfaz adicionales.

</dd> </dl>

NLA implementa la red lógica como una clase de servicio, con un GUID y propiedades de clase asociados. Cada red lógica para la que NLA devuelve información es una instancia de esa clase de servicio.

 

 



