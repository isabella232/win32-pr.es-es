---
title: Reutilizar objetos
description: Reutilizar objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2020
ms.locfileid: "104533081"
---
# <a name="reusing-objects"></a>Reutilizar objetos

Un objetivo importante de cualquier modelo de objetos es permitir que los autores de objetos reutilicen y extiendan objetos proporcionados por otros como partes de sus propias implementaciones. Una manera de hacer esto en Microsoft Visual C++ y en otros lenguajes es mediante la *herencia de implementación*, que permite que un objeto herede ("subclase") algunas de sus funciones de otro objeto y reemplace otras funciones.

El problema de la interacción de objetos en todo el sistema mediante la herencia de implementación tradicional es que el contrato (la interfaz) entre los objetos de una jerarquía de implementación no está claramente definido. De hecho, es implícito y ambiguo. Cuando el objeto primario o secundario cambia su implementación, el comportamiento de los componentes relacionados podría quedar indefinido o implementado sin problemas. En una sola aplicación, donde la implementación puede ser administrada por un único equipo de ingeniería que actualice todos los componentes al mismo tiempo, no siempre es una preocupación importante. En un entorno en el que los componentes de un equipo se crean a través de la reutilización en caja negra de otros componentes creados por otros equipos, este tipo de inestabilidad se arriesga a reutilizar. Además, la herencia de implementación normalmente solo funciona dentro de los límites del proceso. Esto hace que la herencia de implementación tradicional no sea práctica para sistemas grandes y en constante evolución compuestos por componentes de software creados por muchos equipos de ingeniería.

La clave para crear componentes reutilizables es poder tratar el objeto como un cuadro opaco. Esto significa que el fragmento de código que intenta volver a usar otro objeto no sabe nada y no necesita saber nada sobre la estructura interna o la implementación del componente que se está usando. En otras palabras, el código que intenta volver a usar un componente depende del comportamiento del objeto y no de su implementación exacta.

Para lograr una reutilización en negro, COM adopta otros mecanismos de reusabilidad establecidos, como la *contención/delegación* y la *agregación*.

> [!NOTE]  
> Para mayor comodidad, el objeto que se va a reutilizar se denomina *objeto interno* y el objeto que utiliza ese objeto interno es el *objeto externo*.

 

Es importante recordar en ambos mecanismos cómo aparece el objeto externo a sus clientes. En lo que respecta a los clientes, ambos objetos implementan las interfaces en las que el cliente puede obtener un puntero. El cliente trata el objeto externo como un cuadro opaco y, por lo tanto, no tiene que preocuparse por la estructura interna de los objectâ externos, por lo que el cliente solo le preocupa el comportamiento.

Para obtener más información, vea los temas siguientes:

-   [Contención/delegación](containment-delegation.md)
-   [Agregación](aggregation.md)

 

 




