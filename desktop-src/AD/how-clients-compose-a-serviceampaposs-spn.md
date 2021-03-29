---
title: Cómo los clientes componen el SPN de un servicio
description: Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que se debe conectar.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Cómo los clientes componen el SPN de un servicio en AD
- nombre de entidad de seguridad de servicio AD, cómo los clientes componen el SPN de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993897"
---
# <a name="how-clients-compose-a-services-spn"></a>Cómo los clientes componen el SPN de un servicio

Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que se debe conectar. La aplicación cliente puede usar la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN. El cliente especifica los componentes del SPN con datos conocidos o datos recuperados de orígenes distintos del propio servicio.

La forma de un SPN es como se muestra en el formato siguiente:


```C++
<service class>/<host>:<port>/<service name>
```



En este formato, &lt; &gt; se requiere "clase de servicio" y " &lt; host &gt; ". " &lt; Puerto &gt; " y " &lt; nombre de servicio &gt; " opcional.

Normalmente, el cliente reconoce la &lt; parte "clase &gt; de servicio" del nombre y reconoce los componentes opcionales que se van a incluir en el SPN. El cliente puede recuperar componentes del SPN de orígenes como un punto de conexión de servicio (SCP) o una entrada de usuario. Por ejemplo, el cliente puede leer el atributo **serviceDNSName** del SCP de un servicio para obtener el &lt; componente "host &gt; ". El atributo **serviceDNSName** contiene el nombre DNS del servidor en el que se ejecuta la instancia de servicio o el nombre DNS de los registros SRV que contienen los datos de host para las réplicas de servicio. El &lt; componente "nombre del servicio &gt; ", que solo se usa para los servicios replicables, puede ser el nombre distintivo del SCP del servicio, el nombre DNS del dominio atendido por el servicio o el nombre DNS de los registros SRV o mx.

Para obtener más información y un ejemplo de código que se usa para crear un SPN para un servicio, vea [cómo un cliente autentica un servicio de Windows Sockets basado en SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Para obtener más información y una descripción de los componentes de SPN, vea [formatos de nombre para SPN únicos](name-formats-for-unique-spns.md).

 

 




