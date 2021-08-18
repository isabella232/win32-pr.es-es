---
title: Usar Transport-Level seguridad en el cliente
description: El cliente especifica cómo el servidor suplanta al cliente cuando el cliente establece el enlace de cadena.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Llamada a procedimiento remoto RPC , tareas, mediante la seguridad de nivel de transporte en el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee610da50d34711c9ec40f93c29ed08d2bb97ba83c02bc4e8c297b08f859c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010603"
---
# <a name="using-transport-level-security-on-the-client"></a>Usar Transport-Level seguridad en el cliente

El cliente especifica cómo el servidor suplanta al cliente cuando el cliente establece el enlace de cadena. Esta información de QOS se proporciona como una opción de punto de conexión en el enlace de cadena. El cliente puede especificar el nivel de suplantación, el seguimiento dinámico o estático y la marca de solo efectivo.

**Para proporcionar información de calidad de servicio para el servidor**

1.  El cliente llama [**a RpcStringBindingCompose para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) crear las cadenas de componente, incluidas las opciones de punto de conexión, en el contexto de enlace de cadena correcto.
2.  El cliente llama [**a RpcBindingFromStringBinding para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) obtener un nuevo identificador de enlace y aplicar la información de calidad de servicio para el cliente.
3.  El cliente realiza llamadas a procedimientos remotos mediante el identificador .

Microsoft RPC admite Windows de seguridad solo en [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) y [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Se omiten las opciones de seguridad para otros transportes.

El cliente puede asociar los siguientes parámetros de seguridad al enlace para el ncacn de transporte de canalización con nombre [**\_ ncacn np**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identificación, suplantación o Anónima. Especifica el tipo de seguridad utilizado. El valor predeterminado es Impersonation.
-   Dinámica o estática. Determina si la información de seguridad asociada a un subproceso es una copia de la información de seguridad creada en el momento en que se realiza la llamada a procedimiento remoto (estática) o un puntero a la información de seguridad (dinámica).

    La información de seguridad estática no cambia. La configuración dinámica refleja la configuración de seguridad actual, incluidos los cambios realizados después de realizar la llamada al procedimiento remoto. Para [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np), el valor predeterminado para las conexiones de canalización con nombre remotas es estático; para las conexiones de canalización con nombre locales, el valor predeterminado es dinámico.

-   **TRUE** o **FALSE**. Especifica el valor de la marca de solo efectivo. Un valor true **indica** que solo los privilegios de token establecidos en on en el momento de la llamada son efectivos. El valor **FALSE indica** que todos los privilegios están disponibles y que la aplicación puede modificarlos.

Cualquier combinación de esta configuración se puede asignar al enlace, como se muestra en el ejemplo siguiente:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

La configuración predeterminada de los parámetros de seguridad varía según el protocolo de transporte.

Para obtener información adicional sobre la sintaxis de las opciones de punto de conexión, vea [punto de conexión](/windows/desktop/Midl/endpoint).

 

 