---
title: Representación de datos
description: Los entornos informáticos pueden diferir significativamente, como pueden ser las arquitecturas de red.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- RPC (llamada a procedimiento remoto), Descripción y representación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797055"
---
# <a name="data-representation"></a>Representación de datos

Los entornos informáticos pueden diferir significativamente, como pueden ser las arquitecturas de red. Para dar cabida a estas diferencias, MIDL permite modificar la forma de representar los datos. A veces, puede simplificar el desarrollo convirtiendo los datos en un formato que la aplicación pueda controlar más fácilmente. Puede modificar el formato de datos de la aplicación para que se pueda transmitir más eficazmente a través de la red.

Los **\[** atributos [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** y **\[** [**representan \_ como**](/windows/desktop/Midl/represent-as) **\]** indican al compilador que asocie un tipo transmisible que el código auxiliar pasa entre el cliente y el servidor, con un tipo de usuario que usan las aplicaciones cliente y servidor. Debe proporcionar las rutinas que llevan a cabo la conversión entre el tipo de usuario y el tipo transmisible, y las rutinas para liberar la memoria que se usó para almacenar los datos convertidos. El uso del atributo **\[ Transmit \_ as \]** IDL o el atributo **\[ representated \_ as \]** ACF indica al código auxiliar que llame a estas rutinas de conversión antes y después de la transmisión. El **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** permite convertir un tipo de datos en otro tipo de datos para su transmisión a través de la red. El **\[** atributo [**representate \_ as**](/windows/desktop/Midl/represent-as) **\]** le permite controlar el modo en que se presentan los datos de la red a la aplicación.

Los atributos de serialización de **\[** [**conexión \_**](/windows/desktop/Midl/wire-marshal) **\]** y de cálculo de **\[** [**\_ referencias de usuario**](/windows/desktop/Midl/user-marshal) **\]** son extensiones de Microsoft para IDL de OSF-DCE. Su sintaxis y su funcionalidad son similares a las de la transmisión especificada **\[ \_ por DCE \] como** y **\[ representan \_ como \]** atributos, respectivamente. La diferencia es que, en lugar de convertir los datos de un tipo a otro, se serializan los datos directamente. Para ello, debe proporcionar las rutinas externas para ajustar el tamaño del búfer de datos en los lados cliente y servidor, serializar y calcular las referencias de los datos en los lados cliente y servidor, y liberar los datos en el lado servidor. El compilador MIDL genera códigos de formato que indican al motor NDR que llame a estas rutinas externas cuando sea necesario.

Los atributos **\[ \_ serialización \] de conexión** y cálculo de **\[ \_ referencias \] del usuario** permiten calcular las referencias de tipos de datos que, de otro modo, no se pudieron transmitir a través de los límites del proceso. Además, dado que hay menos sobrecarga asociada con la conversión de tipos, las referencias de **\[ conexión \_ \]** y las **\[ \_ referencias \] de usuario** proporcionan un rendimiento mejorado en tiempo de ejecución, en comparación con la **\[ transmisión \_ como \]** y la **\[ representación \_ como \]**. Los atributos de serialización de **\[ conexión \_ \]** y de **\[ cálculo de \_ referencias \] de usuario** se excluyen mutuamente con respecto a los demás y **\[ \_ \]** con respecto a las operaciones de **\[ transmisión \_ \]** y representación como atributos para un tipo determinado.

Es importante tener en cuenta que la implementación de los atributos de serialización de **\[ conexión \_ \]** y de **\[ cálculo de \_ referencias \] del usuario** debe seguir las reglas de serialización dictadas por la especificación de OSF-DCE. Por ese motivo, no se recomienda el uso de estos atributos si no está familiarizado con el protocolo de conexión. Puede encontrar más información sobre la transferencia de sintaxis de NDR en [www.Opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

En esta sección se proporciona una breve descripción de estos elementos para los atributos MIDL, en los temas siguientes:

-   [**Los \_ atributos transmitir como y se representan \_ como**](the-transmit-as-and-represent-as-attributes.md)
-   [**Atributos de serialización de conexión \_ y cálculo de referencias del usuario \_**](the-wire-marshal-and-user-marshal-attributes.md)

 

 