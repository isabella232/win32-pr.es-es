---
description: Después de haber registrado una clase de eventos en el catálogo de COM+, puede Agregar suscriptores a la clase de eventos y las suscripciones a los suscriptores.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registro de una suscripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423443"
---
# <a name="registering-a-subscription"></a>Registro de una suscripción

Después de haber registrado una clase de eventos en el catálogo de COM+, puede Agregar suscriptores a la clase de eventos y las suscripciones a los suscriptores. Las suscripciones se pueden suscribir a un único método o a todos los métodos de una interfaz. Para recibir llamadas en más de un método, pero no en todos los métodos, de una interfaz, debe agregar una suscripción para cada método al que desee recibir una llamada. La herramienta de administración de servicios de componentes puede buscar en el catálogo de COM+ las clases de eventos registradas que admiten las interfaces implementadas por el suscriptor y le ofrece la opción de suscribirse. Elija el publicador que le ofrezca los eventos deseados.

Para agregar suscriptores al componente suscriptor, siga estos pasos:

1.  Después de crear una nueva aplicación COM+ e instalar el componente de suscriptor, haga clic con el botón secundario en la carpeta **suscripciones** para habilitar el Asistente para nueva suscripción com+.

2.  Elija la clase de eventos de la que desea recibir eventos.

3.  Escriba el nombre de la suscripción.

4.  Habilite la suscripción.

5.  Haga clic en **OK**.

Cuando una aplicación de publicador desea activar un evento, el publicador crea una instancia del objeto de la clase de evento y llama a un método en él. COM+ busca en el catálogo de COM+ para encontrar todos los suscriptores. Crea el objeto de suscriptor (directamente, en cola o con un moniker) y pasa la llamada al método realizada originalmente por el publicador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar una clase de eventos](registering-an-event-class.md)
</dt> </dl>

 

 



