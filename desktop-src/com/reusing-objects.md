---
title: Volver ausar objetos
description: Volver ausar objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465968"
---
# <a name="reusing-objects"></a>Volver ausar objetos

Un objetivo importante de cualquier modelo de objetos es permitir que los autores de objetos reutilicen y amplíen los objetos proporcionados por otros como partes de sus propias implementaciones. Una manera de hacerlo en Microsoft Visual C++ y otros lenguajes es mediante la herencia de implementación *,* que permite a un objeto heredar ("subclase") algunas de sus funciones de otro objeto mientras se reemplazan otras funciones.

El problema de la interacción de objetos en todo el sistema mediante la herencia de implementación tradicional es que el contrato (la interfaz) entre los objetos de una jerarquía de implementación no está claramente definido. De hecho, es implícito y ambiguo. Cuando el objeto primario o secundario cambia su implementación, el comportamiento de los componentes relacionados podría quedar indefinido o implementarse de forma inexplicable. En cualquier aplicación, donde la implementación puede administrarse mediante un único equipo de ingeniería que actualiza todos los componentes al mismo tiempo, esto no siempre es un problema importante. En un entorno en el que los componentes de un equipo se construyen a través de la reutilización de caja negra de otros componentes creados por otros equipos, este tipo de inestabilidad pone en peligro la reutilización. Además, la herencia de implementación normalmente solo funciona dentro de los límites del proceso. Esto hace que la herencia de implementación tradicional no sea práctica para sistemas grandes y en constante evolución compuestos por componentes de software creados por muchos equipos de ingeniería.

La clave para crear componentes reutilizables es poder tratar el objeto como un cuadro opaco. Esto significa que el fragmento de código que intenta reutilizar otro objeto no sabe nada y no necesita saber nada sobre la estructura interna o la implementación del componente que se está utilizando. En otras palabras, el código que intenta reutilizar un componente depende del comportamiento del objeto y no de su implementación exacta.

Para lograr la reusabilidad de caja negra, COM adopta otros mecanismos de reusabilidad establecidos, como la *contención/delegación* y la *agregación*.

> [!NOTE]  
> Para mayor comodidad, el objeto  que se reutiliza se denomina objeto interno y el objeto que usa ese objeto interno es *el objeto externo*.

 

Es importante recordar en ambos mecanismos cómo aparece el objeto externo a sus clientes. En lo que respecta a los clientes, ambos objetos implementan las interfaces a las que el cliente puede obtener un puntero. El cliente trata el objeto externo como un cuadro opaco y, por lo tanto, no le importa, ni tiene que importarle, la estructura interna del objeto externo; "el cliente solo se preocupa por el comportamiento.

Para obtener más información, vea los temas siguientes:

-   [Contención y delegación](containment-delegation.md)
-   [Agregación](aggregation.md)

 

 




