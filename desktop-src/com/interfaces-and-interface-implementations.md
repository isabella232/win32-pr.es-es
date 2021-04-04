---
title: Interfaces e implementaciones de interfaz
description: COM hace una distinción fundamental entre las definiciones de interfaz y sus implementaciones.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8df92ac8b851925d82a4b03505fa4c5ab3dc39
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "104077421"
---
# <a name="interfaces-and-interface-implementations"></a>Interfaces e implementaciones de interfaz

COM hace una distinción fundamental entre las definiciones de interfaz y sus implementaciones.

Una *interfaz* es realmente un contrato que está compuesto por un grupo de prototipos de función relacionados cuyo uso se define pero cuya implementación no es. Estos prototipos de función son equivalentes a las clases base virtuales puras en la programación de C++. Una definición de interfaz especifica las funciones miembro de la interfaz, denominadas *métodos*, los tipos de valor devuelto, el número y los tipos de sus parámetros y lo que deben hacer. No hay ninguna implementación asociada a una interfaz.

Una *implementación de interfaz* es el código que proporciona un programador para llevar a cabo las acciones especificadas en una definición de interfaz. Las implementaciones de muchas de las interfaces que un programador puede utilizar en una aplicación basada en objetos se incluyen en las bibliotecas COM. Sin embargo, los programadores pueden omitir estas implementaciones y escribir las suyas propias. Una implementación de interfaz se debe asociar a un objeto cuando se crea una instancia de ese objeto, y la implementación proporciona los servicios que ofrece el objeto.

Por ejemplo, una interfaz hipotética denominada IStack podría definir dos métodos, denominados "Inserte" y "pop", que especifican que las sucesivas llamadas al método Pop devuelven, en orden inverso, los valores pasados previamente al método de envío. Esta definición de interfaz no especificaría cómo se implementarán las funciones en el código. En la implementación de la interfaz, un programador podría implementar la pila como una matriz e implementar los métodos de envío y de extracción de tal forma que tenga acceso a esa matriz, mientras que otro programador podría utilizar una lista vinculada e implementar los métodos en consecuencia. Independientemente de una implementación concreta de los métodos de envío y de extracción, la representación en memoria de un puntero a una interfaz IStack y, por tanto, su uso por parte de un cliente, está determinada completamente por la definición de interfaz.

Los objetos simples solo admiten una interfaz única. Los objetos más complicados, como los objetos que se van a incrustar, suelen admitir varias interfaces. Los clientes tienen acceso a un objeto COM solo a través de un puntero a una de sus interfaces, que, a su vez, permite al cliente llamar a cualquiera de los métodos que componen esa interfaz. Estos métodos determinan cómo un cliente puede utilizar los datos del objeto.

Las interfaces definen un contrato entre un objeto y sus clientes. El contrato especifica los métodos que se deben asociar a cada interfaz y cuál debe ser el comportamiento de cada uno de los métodos en términos de entrada y salida. Normalmente, el contrato no define cómo implementar los métodos en una interfaz. Otro aspecto importante del contrato es que si un objeto admite una interfaz, debe admitir todos los métodos de la interfaz de alguna manera. No todos los métodos de una implementación tienen que hacer algo. Si un objeto no admite la función implícita de un método, su implementación puede ser una devolución simple o quizás el resultado de un mensaje de error significativo, pero los métodos deben existir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




