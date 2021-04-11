---
description: El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que pueden moverse entre distintas redes y para seleccionar configuraciones óptimas cuando hay más de una disponible.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: El rol de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276269"
---
# <a name="the-role-of-nla"></a>El rol de NLA

El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que pueden moverse entre distintas redes y para seleccionar configuraciones óptimas cuando hay más de una disponible. Por ejemplo, un equipo inalámbrico que se itinerancia entre redes físicas puede usar NLA para determinar la configuración adecuada en función de la información sobre la conexión de red disponible. NLA también resulta útil cuando un equipo de host múltiple tiene una conexión física a una red mientras también está conectado a otra red a través de una conexión de acceso telefónico o un túnel.

En el pasado, los desarrolladores tenían que obtener información sobre una interfaz de red lógica y, por lo tanto, tomar decisiones sobre la conectividad de red, en función de una gran cantidad de información de red dispares. En esas circunstancias, los desarrolladores tenían que elegir la interfaz de red adecuada en función de la dirección IP, la subred de la interfaz, el nombre del sistema de nombres de dominio (DNS) asociado a la interfaz, la dirección MAC de una NIC, un nombre de red inalámbrica u otra información de red. NLA reduce este problema proporcionando una interfaz estándar para enumerar la información de los datos adjuntos de la red lógica, correlacionarla con la información de la interfaz de red física y, a continuación, proporcionar una notificación cuando se invalida la información devuelta previamente.

NLA proporciona la siguiente información de ubicación de red:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identidad de red lógica
</dt> <dd>

NLA primero intenta identificar una red lógica por su nombre de dominio DNS. Si una red lógica no tiene un nombre de dominio, NLA identifica la red a partir de la información estática personalizada almacenada en el registro y, por último, de su dirección de subred.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces de red lógica
</dt> <dd>

Para cada red a la que está conectado un equipo, NLA proporciona un *AdapterName* que identifica de forma única una interfaz física como una NIC o una interfaz lógica como una conexión RAS. A continuación, AdapterName se puede usar con las funciones disponibles en la API auxiliar de IP para obtener más características de la interfaz.

</dd> </dl>

NLA implementa la red lógica como una clase de servicio, con una propiedad y un GUID de clase asociados. Cada red lógica para la que NLA devuelve información es una instancia de esa clase de servicio.

 

 



