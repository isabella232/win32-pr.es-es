---
title: Representación de datos
description: Los entornos informáticos pueden diferir significativamente, al igual que las arquitecturas de red.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Llamada a procedimiento remoto RPC, descrita, representación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259807"
---
# <a name="data-representation"></a>Representación de datos

Los entornos informáticos pueden diferir significativamente, al igual que las arquitecturas de red. Para dar cabida a estas diferencias, MIDL permite modificar la forma en que se representan los datos. A veces puede simplificar el desarrollo mediante la conversión de datos en un formato que la aplicación pueda controlar más fácilmente. Puede modificar el formato de datos de la aplicación para que se pueda transmitir de forma más eficaz a través de la red.

Los atributos transmitir como y representar como indica al compilador que asocie un tipo **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** **\[** [**\_**](/windows/desktop/Midl/represent-as) transmisible que el código auxiliar pasa entre el cliente y el servidor, con un tipo de usuario que usan las aplicaciones cliente y **\]** servidor. Debe proporcionar las rutinas que llevan a cabo la conversión entre el tipo de usuario y el tipo transmisible, y las rutinas para liberar la memoria que se usó para contener los datos convertidos. El uso **\[ de la transmisión \_ como \]** atributo IDL o **\[ la \_ \]** representación como atributo ACF indica al código auxiliar que llame a estas rutinas de conversión antes y después de la transmisión. El **\[** [**atributo transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** permite convertir un tipo de datos en otro tipo de datos para la transmisión a través de la red. El atributo represent as permite controlar la forma en que se presentan los datos de la red a la **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** aplicación.

Los **\[** [**atributos wire \_ marshal**](/windows/desktop/Midl/wire-marshal) **\]** y user **\[** [**\_ marshal**](/windows/desktop/Midl/user-marshal) **\]** son extensiones de Microsoft para el IDL de OSF-DCE. Su sintaxis y funcionalidad son similares a las de la transmisión especificada por DCE **\[ \_ \]** como y **\[ representan \_ como \]** atributos, respectivamente. La diferencia es que, en lugar de convertir los datos de un tipo a otro, serializa los datos directamente. Para ello, debe proporcionar las rutinas externas para cambiar el tamaño del búfer de datos en los lados cliente y servidor, serializar y desmarque los datos en los lados cliente y servidor, y liberar los datos en el lado servidor. El compilador MIDL genera códigos de formato que instruyen al motor QR que llame a estas rutinas externas cuando sea necesario.

Los **\[ atributos wire marshal \_ y \]** **\[ user \_ marshal \]** hacen posible serializar tipos de datos que, de lo contrario, no se podían transmitir a través de los límites del proceso. Además, dado que hay menos sobrecarga asociada a la conversión de **\[ \_ \]** **\[ \_ \] tipos,** la serialización de conexión y la serialización de usuario proporcionan un rendimiento mejorado en tiempo de ejecución, **\[ \_ \]** en comparación con transmitir como y **\[ representar \_ como \]**. Los **\[ atributos wire \_ marshal \]** y user **\[ \_ marshal \]** son mutuamente **\[ \_ \]** **\[ \_ \]** excluyentes entre sí y con respecto a la transmisión como y representan como atributos para un tipo determinado.

Es importante tener en cuenta que la implementación de los atributos wire **\[ \_ marshal \]** y **\[ user \_ marshal \]** debe seguir las reglas de serialización dictadas por la especificación OSF-DCE. Por ese motivo, no se recomienda el uso de estos atributos si no está familiarizado con el protocolo de conexión. Puede encontrar más información sobre la transferencia de sintaxis de QL [en www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

En esta sección se proporciona una breve introducción a estos atributos de MIDL, en los temas siguientes:

-   [**Transmitir \_ como y representar \_ como atributos**](the-transmit-as-and-represent-as-attributes.md)
-   [**Atributos de \_ referencias de conexión y referencias de \_ usuario**](the-wire-marshal-and-user-marshal-attributes.md)

 

 