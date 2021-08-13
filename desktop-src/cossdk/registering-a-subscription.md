---
description: Después de haber registrado una clase de eventos en el catálogo de COM+, puede agregar suscriptores a la clase de eventos y suscripciones a los suscriptores.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registro de una suscripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f152834c805bd905019d2afe0e353c0a962452c32ef144cc3c3d445b59fbbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547115"
---
# <a name="registering-a-subscription"></a>Registro de una suscripción

Después de haber registrado una clase de eventos en el catálogo de COM+, puede agregar suscriptores a la clase de eventos y suscripciones a los suscriptores. Las suscripciones pueden suscribirse a un único método o a todos los métodos de una interfaz. Para recibir llamadas en más de un método , pero no en todos los métodos, de una interfaz, debe agregar una suscripción para cada método al que desee recibir una llamada. La herramienta de administración Servicios de componentes puede buscar en el catálogo de COM+ clases de eventos registradas que admitan las interfaces implementadas por el suscriptor y le ofrece la opción de suscribirse. Elija el publicador que le ofrece los eventos deseados.

Para agregar suscriptores al componente de suscriptor, siga estos pasos:

1.  Después de crear una nueva aplicación COM+ e instalar el componente de suscriptor, haga clic con el botón derecho en la carpeta **Suscripciones** para habilitar el Asistente para nueva suscripción de COM+.

2.  Elija la clase de eventos de la que desea recibir eventos.

3.  Escriba el nombre de la suscripción.

4.  Habilite la suscripción.

5.  Haga clic en **Aceptar**.

Cuando una aplicación de publicador quiere abrir un evento, el publicador crea una instancia del objeto de clase de evento y llama a un método en él. COM+ busca en el catálogo de COM+ para buscar todos los suscriptores. Crea el objeto de suscriptor (directamente, en cola o con un moniker) y pasa la llamada al método realizada originalmente por el publicador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una clase de eventos](registering-an-event-class.md)
</dt> </dl>

 

 



