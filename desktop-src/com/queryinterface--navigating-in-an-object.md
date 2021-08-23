---
title: Navegación de QueryInterface en un objeto
description: Navegación de QueryInterface en un objeto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbb25f76f87b43f6fc4fc4d3a1a3eb65c19960942769818a83f176fc62f72c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611075"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: Navegar en un objeto

Después de tener un puntero inicial a una interfaz en un objeto, COM tiene un mecanismo muy sencillo para averiguar si el objeto admite otra interfaz específica y, si es así, para obtener un puntero a él. (Para obtener información sobre cómo obtener un puntero inicial a una interfaz en un objeto , vea [Obtener un puntero a un objeto](getting-a-pointer-to-an-object.md)). Este mecanismo es el [**método QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**la interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Si el objeto admite la interfaz solicitada, el método debe devolver un puntero a esa interfaz. Esto permite que un objeto navegue libremente a través de las interfaces que admite un objeto. **QueryInterface** separa la solicitud "¿Se admite un contrato determinado?" del uso de alto rendimiento de ese contrato una vez que las negociaciones se han realizado correctamente.

Cuando un cliente obtiene inicialmente acceso a un objeto, ese cliente recibirá, como mínimo, un puntero de interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (la interfaz más fundamental) a través del cual puede controlar la duración del objeto ( al indiciar al objeto cuando haya terminado con el objeto ) e invocar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). El cliente está programado para pedir a cada objeto que administra que realice algunas operaciones, pero la **interfaz IUnknown** no tiene ninguna función para esas operaciones. En su lugar, esas operaciones se expresan a través de otras interfaces. Por lo tanto, el cliente está programado para negociar con objetos para esas interfaces. En concreto, el cliente llamará **a QueryInterface** para solicitar a un objeto una interfaz a través de la cual el cliente pueda invocar las operaciones deseadas.

Dado que el objeto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), tiene la capacidad de aceptar o rechazar la solicitud. Si el objeto acepta la solicitud del cliente, **QueryInterface** devuelve un nuevo puntero a la interfaz solicitada al cliente. A través de ese puntero de interfaz, el cliente tiene acceso a los métodos de esa interfaz. Por otro lado, si el objeto rechaza la solicitud del cliente, **QueryInterface** devuelve un puntero nulo (un error) y el cliente no tiene ningún puntero a través del cual llamar a las funciones deseadas. En este caso, el cliente debe tratar correctamente esa posibilidad. Por ejemplo, suponga que un cliente tiene un puntero a la interfaz A en un objeto y solicita las interfaces B y C. Supongamos también que el objeto admite la interfaz B, pero no admite la interfaz C. El resultado es que el objeto devuelve un puntero a B e informa de que no se admite C.

Un punto clave es que cuando un objeto rechaza una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), es imposible que el cliente pida al objeto que realice las operaciones expresadas a través de la interfaz solicitada. Un cliente debe tener un puntero de interfaz para invocar métodos en esa interfaz. Si el objeto se rehúsa a proporcionar el puntero solicitado, el cliente debe estar preparado para hacerlo, ya sea no haciendo lo que tenía pensado hacer con ese objeto o intentando volver a usar otra interfaz, quizás menos eficaz. Esta característica de la funcionalidad COM funciona bien en comparación con otros sistemas orientados a objetos en los que no se puede saber si una función funcionará hasta que llame a esa función e, incluso entonces, no se puede controlar el error. **QueryInterface** proporciona una manera confiable y coherente de saber si un objeto admite una interfaz antes de intentar llamar a sus métodos.

El [**método QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) también proporciona una manera sólida y confiable para que un objeto indique que no admite un contrato determinado. Es decir, si en una llamada a **QueryInterface** se le pregunta a un objeto "antiguo" si admite una interfaz "nueva" (una, por ejemplo, que se creó después de enviar el objeto antiguo), el objeto antiguo responderá de forma confiable, sin causar un bloqueo, "no". La tecnología que lo admite es el algoritmo por el que se asignan los IID. Aunque esto puede parecer un punto pequeño, es muy importante para la arquitectura general del sistema y la capacidad de consultar elementos heredados sobre la nueva funcionalidad es, sorprendentemente, una característica que no está presente en la mayoría de las demás arquitecturas de objetos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso e implementación de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




