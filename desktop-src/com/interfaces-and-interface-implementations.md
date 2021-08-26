---
title: Interfaces e implementaciones de interfaz
description: COM hace una distinción fundamental entre las definiciones de interfaz y sus implementaciones.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee00521b847acbd063f1cd7ad84a0eb231f78d7bd274b7a4658996dbdd61150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992705"
---
# <a name="interfaces-and-interface-implementations"></a>Interfaces e implementaciones de interfaz

COM hace una distinción fundamental entre las definiciones de interfaz y sus implementaciones.

Una *interfaz* es realmente un contrato que consta de un grupo de prototipos de función relacionados cuyo uso está definido pero cuya implementación no es . Estos prototipos de función son equivalentes a las clases base virtuales puras en la programación de C++. Una definición de interfaz especifica las funciones miembro de la interfaz, denominadas métodos *,* sus tipos de valor devuelto, el número y los tipos de sus parámetros y lo que deben hacer. No hay ninguna implementación asociada a una interfaz.

Una *implementación de interfaz* es el código que proporciona un programador para llevar a cabo las acciones especificadas en una definición de interfaz. Las implementaciones de muchas de las interfaces que un programador puede usar en una aplicación basada en objetos se incluyen en las bibliotecas COM. Sin embargo, los programadores pueden omitir estas implementaciones y escribir las suyas propias. Una implementación de interfaz se va a asociar a un objeto cuando se crea una instancia de ese objeto y la implementación proporciona los servicios que ofrece el objeto.

Por ejemplo, una interfaz hipotética denominada IStack podría definir dos métodos, denominados Push y Pop, especificando que las llamadas sucesivas al método Pop devuelven, en orden inverso, valores pasados previamente al método Push. Esta definición de interfaz no especificaría cómo se implementarán las funciones en el código. Al implementar la interfaz, un programador podría implementar la pila como una matriz e implementar los métodos Push y Pop de tal manera que accedan a esa matriz, mientras que otro programador podría usar una lista vinculada e implementar los métodos en consecuencia. Independientemente de una implementación determinada de los métodos Push y Pop, la representación en memoria de un puntero a una interfaz IStack y, por tanto, su uso por parte de un cliente, viene determinada completamente por la definición de la interfaz.

Los objetos simples solo admiten una sola interfaz. Los objetos más complicados, como los objetos insertables, normalmente admiten varias interfaces. Los clientes tienen acceso a un objeto COM solo a través de un puntero a una de sus interfaces, lo que, a su vez, permite al cliente llamar a cualquiera de los métodos que la conste. Estos métodos determinan cómo un cliente puede usar los datos del objeto.

Las interfaces definen un contrato entre un objeto y sus clientes. El contrato especifica los métodos que se deben asociar a cada interfaz y cuál debe ser el comportamiento de cada uno de los métodos en términos de entrada y salida. Por lo general, el contrato no define cómo implementar los métodos en una interfaz . Otro aspecto importante del contrato es que si un objeto admite una interfaz, debe admitir todos los métodos de esa interfaz de alguna manera. No todos los métodos de una implementación necesitan hacer algo. Si un objeto no admite la función implícita por un método, su implementación puede ser una simple devolución o quizás la devolución de un mensaje de error significativo, pero los métodos deben existir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos COM e interfaces](com-objects-and-interfaces.md)
</dt> </dl>

 

 




