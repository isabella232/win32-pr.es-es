---
description: Activación de colas de componentes
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Activación de colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca15be15920ff4745fcec5e57bba6d9e5f33cd65c0559e8c9ed9e00cefb5bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917620"
---
# <a name="activating-component-queues"></a>Activación de colas de componentes

La realización de llamadas a métodos en un componente en cola no ejecuta directamente el método . En su lugar, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) serializa y almacena las llamadas a métodos y los parámetros en una cola donde el componente en cola los recupera y ejecuta posteriormente. A diferencia de la activación de un objeto DCOM remoto, no se crea una instancia del componente en cola cuando se llama a un método. Esta es la idea básica detrás del uso de componentes en cola: no es necesario crear instancias de los componentes en cola al mismo tiempo que la aplicación que realiza la llamada.

> [!Note]  
> En las descripciones para activar una aplicación en cola se supone que la aplicación está marcada como en cola y que la casilla del agente de escucha está habilitada.

 

Puede usar scripting para iniciar y detener una aplicación en cola. Puede colocar el script bajo el control del programador de tareas para ejecutarlo según sea necesario. Por ejemplo, el script se puede ejecutar al reiniciar el sistema si las aplicaciones van a estar disponibles permanentemente. Si la aplicación va a procesar transacciones en modo por lotes, el script se puede ejecutar a una hora determinada cada día junto con un script de apagado para asegurarse de que el procesamiento por lotes se detiene en un momento específico.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para iniciar una aplicación en cola, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Haga clic con el botón derecho en la aplicación cuya cola desea activar.

3.  Haga clic en **Iniciar**.

## <a name="visual-basic"></a>Visual Basic

Consulte el ejemplo COMAdminCatalog.StartApplication.

## <a name="cc"></a>C/C++

Vea el [**ejemplo ICOMAdminCatalog::StartApplication.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Moniker de cola](using-the-queue-moniker.md)
</dt> </dl>

 

 



