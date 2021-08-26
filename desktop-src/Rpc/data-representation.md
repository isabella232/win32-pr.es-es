---
title: Representación de datos
description: Los entornos informáticos pueden diferir significativamente, al igual que las arquitecturas de red.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Llamada a procedimiento remoto RPC , descrita, representación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9a0af96249c356f171396eaf52f91c5e33005eda080929cfbd8eecde27ffa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022095"
---
# <a name="data-representation"></a>Representación de datos

Los entornos informáticos pueden diferir significativamente, al igual que las arquitecturas de red. Para dar cabida a estas diferencias, MIDL permite modificar la forma en que se representan los datos. A veces puede simplificar el desarrollo mediante la conversión de datos en un formato que la aplicación pueda controlar más fácilmente. Puede modificar el formato de datos de la aplicación para que se pueda transmitir de forma más eficaz a través de la red.

La transmisión como y representan como atributos indica al compilador que asocie un tipo **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** **\[** [**\_**](/windows/desktop/Midl/represent-as) transmisible que el código auxiliar pasa entre el cliente y el servidor, con un tipo de usuario que usan las aplicaciones cliente y **\]** servidor. Debe proporcionar las rutinas que llevan a cabo la conversión entre el tipo de usuario y el tipo transmisible, y las rutinas para liberar la memoria que se usó para contener los datos convertidos. El uso **\[ de la transmisión \_ como \]** atributo IDL **\[ \_ \]** o la representación como atributo ACF indica al código auxiliar que llame a estas rutinas de conversión antes y después de la transmisión. El **\[** [**atributo transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** permite convertir un tipo de datos en otro tipo de datos para su transmisión a través de la red. El atributo representar como permite controlar la forma en que los datos de la red se presentan a la **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** aplicación.

Los **\[** [**atributos wire \_ marshal**](/windows/desktop/Midl/wire-marshal) **\]** y user **\[** [**\_ marshal**](/windows/desktop/Midl/user-marshal) **\]** son extensiones de Microsoft para el IDL de OSF-DCE. Su sintaxis y funcionalidad son similares a las de la transmisión especificada por DCE **\[ \_ \]** como y **\[ se representan \_ como \]** atributos, respectivamente. La diferencia es que, en lugar de convertir los datos de un tipo a otro, serializa los datos directamente. Para ello, debe proporcionar las rutinas externas para cambiar el tamaño del búfer de datos en los lados cliente y servidor, serializar y desmarque los datos en los lados cliente y servidor, y liberar los datos en el lado servidor. El compilador MIDL genera códigos de formato que instruyen al motor JPEG que llame a estas rutinas externas cuando sea necesario.

Los **\[ atributos wire marshal \_ y \]** **\[ user \_ marshal \]** hacen posible serializar los tipos de datos que, de lo contrario, no se podrían transmitir a través de los límites del proceso. Además, dado que hay menos sobrecarga asociada a la conversión de **\[ \_ \]** **\[ \_ \] tipos,** las referencias de conexión y las referencias de usuario proporcionan un rendimiento mejorado en tiempo de ejecución, **\[ \_ \]** en comparación con transmitir como y **\[ representar \_ como \]**. Los **\[ atributos wire \_ marshal \]** y **\[ user \_ marshal \]** **\[ \_ \]** **\[ \_ se excluyen mutuamente entre sí y con respecto a la transmisión como y se representan como atributos para un tipo determinado. \]**

Es importante tener en cuenta que la **\[ \_ \]** **\[ \_ \]** implementación de los atributos de serialización de conexión y de serialización de usuario debe seguir las reglas de serialización dictadas por la especificación de OSF-DCE. Por ese motivo, no se recomienda el uso de estos atributos si no está familiarizado con el protocolo de conexión. Puede encontrar más información sobre la transferencia de sintaxis de QL [en www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

En esta sección se proporciona una breve introducción a estos atributos de MIDL, en los temas siguientes:

-   [**Transmitir como \_ y representar \_ como atributos**](the-transmit-as-and-represent-as-attributes.md)
-   [**Atributos de \_ serialización de conexión \_ y de referencias de usuario**](the-wire-marshal-and-user-marshal-attributes.md)

 

 