---
title: Cómo los clientes componen el SPN de un servicio
description: Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que debe conectarse.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Cómo los clientes componen el AD de SPN de un servicio
- nombre de entidad de seguridad de servicio ad , cómo los clientes componen el SPN de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188190"
---
# <a name="how-clients-compose-a-services-spn"></a>Cómo los clientes componen el SPN de un servicio

Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que debe conectarse. La aplicación cliente puede usar la [**función DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN. El cliente especifica los componentes del SPN mediante datos conocidos o datos recuperados de orígenes distintos del propio servicio.

El formato de un SPN es como se muestra en el formulario siguiente:


```C++
<service class>/<host>:<port>/<service name>
```



En este formato, se requieren " &lt; service class " y " host &gt; &lt; &gt; ". " &lt; port " y " service name " &gt; &lt; &gt; opcional.

Normalmente, el cliente reconoce la parte " clase de servicio " del nombre y reconoce cuáles de los componentes opcionales que se &lt; &gt; incluirán en el SPN. El cliente puede recuperar componentes del SPN de orígenes como un punto de conexión de servicio (SCP) o la entrada del usuario. Por ejemplo, el cliente puede leer el atributo **serviceDNSName** del SCP de un servicio para obtener el &lt; componente &gt; "host". El **atributo serviceDNSName** contiene el nombre DNS del servidor en el que se ejecuta la instancia de servicio o el nombre DNS de los registros SRV que contienen los datos del host para las réplicas de servicio. El componente "nombre de servicio", que solo se usa para los servicios replicables, puede ser el nombre distintivo del SCP del servicio, el nombre DNS del dominio al que sirve el servicio o el nombre DNS de los registros SRV o &lt; &gt; MX.

Para obtener más información y un ejemplo de código utilizado para crear un SPN para un servicio, vea [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Para obtener más información y una descripción de los componentes de SPN, vea [Formatos de nombre para SPN únicos.](name-formats-for-unique-spns.md)

 

 




