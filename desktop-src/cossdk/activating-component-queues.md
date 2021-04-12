---
description: Activación de colas de componentes
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Activación de colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423320"
---
# <a name="activating-component-queues"></a>Activación de colas de componentes

La realización de llamadas a métodos en un componente en cola no ejecuta directamente el método. En su lugar, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) calcula las referencias y almacena llamadas y parámetros de métodos en una cola en la que más adelante se recuperan y ejecutan mediante el componente en cola. A diferencia de la activación de un objeto DCOM remoto, no se crea una instancia del componente en cola cuando se llama a un método. Esta es la idea básica detrás del uso de componentes en cola; no es necesario crear instancias de los componentes en cola al mismo tiempo que la aplicación que realiza la llamada.

> [!Note]  
> En las descripciones para activar una aplicación en cola se supone que la aplicación está marcada como en cola y que la casilla del agente de escucha está habilitada.

 

Puede usar scripts para iniciar y detener una aplicación en cola. Puede colocar el script bajo el control del programador de tareas para ejecutarlo según sea necesario. Por ejemplo, el script se puede ejecutar en el reinicio del sistema si las aplicaciones están disponibles de forma permanente. Si la aplicación va a procesar transacciones en modo por lotes, el script se puede ejecutar en un momento determinado cada día junto con un script de cierre para asegurarse de que el procesamiento por lotes se detiene en un momento determinado.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para iniciar una aplicación en cola, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Haga clic con el botón secundario en la aplicación cuya cola desee activar.

3.  Haga clic en **Iniciar**.

## <a name="visual-basic"></a>Visual Basic

Vea el ejemplo de COMAdminCatalog. StartApplication.

## <a name="cc"></a>C/C++

Vea el ejemplo [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el moniker de cola](using-the-queue-moniker.md)
</dt> </dl>

 

 



