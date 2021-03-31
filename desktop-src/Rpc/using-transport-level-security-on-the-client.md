---
title: Usar la seguridad de Transport-Level en el cliente
description: El cliente especifica el modo en que el servidor suplanta al cliente cuando el cliente establece el enlace de cadenas.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de la seguridad de nivel de transporte en el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995551"
---
# <a name="using-transport-level-security-on-the-client"></a>Usar la seguridad de Transport-Level en el cliente

El cliente especifica el modo en que el servidor suplanta al cliente cuando el cliente establece el enlace de cadenas. Esta información de QOS se proporciona como una opción de extremo en el enlace de cadenas. El cliente puede especificar el nivel de suplantación, seguimiento dinámico o estático y la marca de solo efectivo.

**Para proporcionar información de calidad de servicio para el servidor**

1.  El cliente llama a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) para crear las cadenas de componentes, incluidas las opciones de punto de conexión, en el contexto de enlace de cadena correcto.
2.  El cliente llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener un nuevo identificador de enlace y aplicar la información de calidad de servicio para el cliente.
3.  El cliente realiza llamadas a procedimientos remotos mediante el identificador.

Microsoft RPC solo admite características de seguridad de Windows en [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) y [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Se omiten las opciones de seguridad para otros transportes.

El cliente puede asociar los siguientes parámetros de seguridad al enlace para el transporte de canalización con nombre [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identificación, suplantación o anónima. Especifica el tipo de seguridad que se usa. El valor predeterminado es la suplantación.
-   Dinámica o estática. Determina si la información de seguridad asociada a un subproceso es una copia de la información de seguridad creada en el momento en que se realiza la llamada a procedimiento remoto (estática) o un puntero a la información de seguridad (dinámica).

    La información de seguridad estática no cambia. La configuración dinámica refleja la configuración de seguridad actual, incluidos los cambios realizados después de realizar la llamada a procedimiento remoto. En el caso de [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), el valor predeterminado para las conexiones remotas de canalización con nombre es estático, para las conexiones de canalización con nombre local, el valor predeterminado es dinámico.

-   **True** o **false**. Especifica el valor de la marca de solo efectivo. Un valor de **true** indica que solo los privilegios de token establecidos en on en el momento de la llamada son efectivos. Un valor de **false** indica que todos los privilegios están disponibles y que la aplicación puede modificarlos.

Cualquier combinación de estas opciones se puede asignar al enlace, tal y como se muestra en el ejemplo siguiente:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

La configuración predeterminada de los parámetros de seguridad varía según el protocolo de transporte.

Para obtener más información sobre la sintaxis de las opciones del punto de conexión, vea [punto de conexión](/windows/desktop/Midl/endpoint).

 

 