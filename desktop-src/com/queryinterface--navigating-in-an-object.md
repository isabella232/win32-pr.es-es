---
title: Desplazarse por QueryInterface en un objeto
description: Desplazarse por QueryInterface en un objeto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dbd44d200bf0a992f47bc375d0782bdadacf6a3
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104358619"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: desplazarse por un objeto

Después de tener un puntero inicial a una interfaz en un objeto, COM tiene un mecanismo muy sencillo para averiguar si el objeto es compatible con otra interfaz específica y, en caso afirmativo, obtener un puntero a él. (Para obtener información sobre cómo obtener un puntero inicial a una interfaz en un objeto, vea [obtener un puntero a un objeto](getting-a-pointer-to-an-object.md)). Este mecanismo es el método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Si el objeto admite la interfaz solicitada, el método debe devolver un puntero a esa interfaz. Esto permite que un objeto navegue libremente a través de las interfaces que admite un objeto. **QueryInterface** separa la solicitud "¿se admite un contrato determinado?" desde el uso de alto rendimiento de ese contrato una vez que las negociaciones se hayan realizado correctamente.

Cuando un cliente obtiene acceso inicialmente a un objeto, ese cliente recibirá, como mínimo, un puntero de interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (la interfaz más fundamental) a través de la cual puede controlar la duración del objeto. para ello, indique el objeto cuando se realice mediante el objeto e invoque [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). El cliente está programado para preguntar a cada objeto que administra para realizar algunas operaciones, pero la interfaz **IUnknown** no tiene funciones para esas operaciones. En su lugar, esas operaciones se expresan a través de otras interfaces. Por tanto, el cliente está programado para negociar con objetos de esas interfaces. En concreto, el cliente llamará a **QueryInterface** para solicitar un objeto para una interfaz a través de la cual el cliente pueda invocar las operaciones deseadas.

Dado que el objeto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), tiene la capacidad de aceptar o rechazar la solicitud. Si el objeto acepta la solicitud del cliente, **QueryInterface** devuelve un nuevo puntero a la interfaz solicitada al cliente. A través de ese puntero de interfaz, el cliente tiene acceso a los métodos de esa interfaz. Por otro lado, si el objeto rechaza la solicitud del cliente, **QueryInterface** devuelve un puntero nulo (un error) y el cliente no tiene ningún puntero a través del que llamar a las funciones deseadas. En este caso, el cliente debe tratar correctamente la posibilidad. Por ejemplo, suponga que un cliente tiene un puntero a la interfaz a en un objeto y solicita las interfaces B y C. suponga también que el objeto admite la interfaz B pero no admite la interfaz C. El resultado es que el objeto devuelve un puntero a B y notifica que C no se admite.

Un punto clave es que cuando un objeto rechaza una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), no es posible que el cliente solicite al objeto que realice las operaciones expresadas a través de la interfaz solicitada. Un cliente debe tener un puntero de interfaz para invocar métodos en esa interfaz. Si el objeto rechaza proporcionar el puntero solicitado, el cliente debe estar preparado para llevar a cabo sin, ya sea no haciendo lo que tenía previsto hacer con ese objeto o intentando revertir a otra interfaz, quizás menos eficaz. Esta característica de la funcionalidad COM funciona bien en comparación con otros sistemas orientados a objetos en los que no puede saber si una función funcionará hasta que llame a esa función, e incluso después, el control de errores es cierto. **QueryInterface** proporciona una forma confiable y coherente de saber si un objeto admite una interfaz antes de intentar llamar a sus métodos.

El método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) también proporciona una forma sólida y confiable de que un objeto indique que no admite un contrato determinado. Es decir, si en una llamada a **QueryInterface** se le pide un objeto "antiguo", ya sea compatible con una interfaz "nueva" (por ejemplo, que se ha inventado después de que se haya enviado el objeto anterior), el objeto antiguo será confiable, sin provocar un bloqueo, responder "no". La tecnología que es compatible con este es el algoritmo por el que se asignan IID. Aunque esto puede parecer un punto pequeño, es sumamente importante para la arquitectura global del sistema y la capacidad de consultar los elementos heredados sobre la nueva funcionalidad es, sorprendentemente, una característica que no está presente en la mayoría de las demás arquitecturas de objetos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar e implementar IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




