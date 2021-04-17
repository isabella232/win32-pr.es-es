---
description: Una aplicación que contiene al menos un componente queuable se puede marcar como en cola mediante la herramienta administrativa Servicios de componentes.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Crear colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705305"
---
# <a name="creating-component-queues"></a>Crear colas de componentes

Una aplicación que contiene al menos un componente queuable se puede marcar como en cola mediante la herramienta administrativa Servicios de componentes.

Cuando una aplicación se marca como en cola, COM+ crea automáticamente una cola de Message Queue Server para ella. El nombre de la cola es el nombre de la aplicación; Si el nombre de la cola coincide con el nombre de una cola existente, COM+ usará la cola existente.

> [!Note]  
> El parámetro *PathName* de Message Queue Server es una combinación del nombre del servidor remoto (RSN) y el nombre de la aplicación com+. El RSN hace referencia al destino de una activación remota. El RSN se especifica durante la instalación de una aplicación exportable de cliente en un equipo cliente. El procedimiento de instalación utiliza el RSN para dirigir la activación a un equipo cliente especificado. Para obtener más información acerca de los nombres de cola, consulte la tabla de parámetros en la sección "parámetros de moniker de cola" de [Using the Queue moniker](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para especificar una aplicación COM+ como en cola, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Haga clic con el botón secundario en la aplicación para la que desea crear una cola y, a continuación, haga clic en **propiedades**.

3.  Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.

4.  Active la casilla de verificación con la etiqueta **en cola: esta aplicación puede ser accesible mediante colas de MSMQ**.

    > [!Note]  
    > Si la casilla de verificación **en cola** está atenuada, la aplicación no contiene ningún componente queuable.

     

5.  Haga clic en **OK**.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="remarks"></a>Observaciones

Las colas creadas por la biblioteca de administración de COM+ o la herramienta administrativa Servicios de componentes se marcan con el atributo transaccional de Message Queue Server.

Después de instalar una aplicación en cola en el servidor, se puede poner a disposición de los clientes mediante la exportación de la aplicación y la posterior importación de la aplicación en cada cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de componentes de Queuable](creating-queuable-components.md)
</dt> <dt>

[Arquitectura de componentes en cola](queued-components-architecture.md)
</dt> </dl>

 

 



