---
title: Eventos de objetos COM y conectables
description: Cuando un programa detecta algo que ha sucedido, puede notificar a sus clientes.
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104077236"
---
# <a name="events-in-com-and-connectable-objects"></a>Eventos de objetos COM y conectables

Cuando un programa detecta algo que ha sucedido, puede notificar a sus clientes. Por ejemplo, si un programa de cotización bursátil detecta un cambio en el precio de una acción, puede notificar a todos los clientes el cambio. Este proceso de notificación se conoce como *activación de un evento*.

Con COM, los objetos de servidor pueden utilizar eventos COM para desencadenar eventos sin información sobre los objetos a los que se va a notificar. Los objetos también pueden usar *objetos conectables* para mantener información detallada acerca de los clientes que han solicitado las notificaciones.

Los objetos conectables COM proporcionan interfaces de salida a sus clientes además de las interfaces de entrada. Como resultado, los objetos y sus clientes pueden interactuar en la comunicación bidireccional. Las interfaces de entrada se implementan en un objeto y reciben llamadas de clientes externos de un objeto, mientras que las interfaces salientes se implementan en el receptor del cliente y reciben llamadas del objeto. El objeto define una interfaz que desea usar y el cliente la implementa.

Un objeto define sus interfaces de entrada y proporciona implementaciones de estas interfaces. Las interfaces de entrada están disponibles para los clientes a través del método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) del objeto. Los clientes llaman a los métodos de una interfaz entrante en el objeto y el objeto realiza las acciones deseadas en nombre del cliente.

Las interfaces de salida también se definen mediante un objeto, pero el cliente proporciona las implementaciones de las interfaces de salida en un objeto receptor que crea el cliente. A continuación, el objeto llama a los métodos de la interfaz de salida en el objeto receptor para notificar al cliente los cambios en el objeto, para desencadenar eventos en el cliente, para solicitar algo del cliente o, de hecho, para cualquier propósito con el que se encuentre el creador del objeto.

Un ejemplo de una interfaz de salida es una interfaz IButtonSink definida por un control de botón de control para notificar sus eventos a sus clientes. Por ejemplo, el objeto de botón llama a IButtonSink:: OnClick en el objeto receptor del cliente cuando el usuario hace clic en el botón de la pantalla. El control de botón define la interfaz de salida. Para que un cliente del botón controle el evento, el cliente debe implementar esa interfaz de salida en un objeto receptor y, a continuación, conectar ese receptor al control de botón. A continuación, cuando se produzcan eventos en el botón, el botón llamará al receptor, momento en el cual el cliente puede ejecutar cualquier acción que desee asignar a ese botón.

Los objetos conectables proporcionan un mecanismo general para la comunicación de objeto a cliente. Cualquier objeto que desee exponer eventos o notificaciones de cualquier tipo puede utilizar esta tecnología. Además de la tecnología de objetos conectables generales, COM proporciona muchas interfaces de sitio y receptor de propósito especial usadas por los objetos para notificar a los clientes de eventos específicos de interés para el cliente. Por ejemplo, se puede usar [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) en los objetos para notificar a los clientes los datos y ver los cambios en el objeto.

Para obtener más información, vea los temas siguientes:

-   [Arquitectura de objetos conectables](architecture-of-connectable-objects.md)
-   [Interfaces de objeto conectables](connectable-object-interfaces.md)

 

 




