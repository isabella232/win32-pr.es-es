---
description: Una aplicación que contiene al menos un componente que se puede poner en cola se puede marcar como en cola mediante la herramienta administrativa de servicios de componentes.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Crear colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c44f670cea15e1cb1a4549d5c1e847956eb41d400ae01d557803dbd1ce2b439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793465"
---
# <a name="creating-component-queues"></a>Crear colas de componentes

Una aplicación que contiene al menos un componente que se puede poner en cola se puede marcar como en cola mediante la herramienta administrativa de servicios de componentes.

Cuando una aplicación se marca como en cola, COM+ crea automáticamente una cola de cola de mensajes para ella. El nombre de la cola es el nombre de la aplicación; si el nombre de la cola coincide con el nombre de una cola existente, COM+ usará la cola existente.

> [!Note]  
> El parámetro *PathName* de Message Queuing es una combinación del nombre del servidor remoto (RSN) y el nombre de la aplicación COM+. El RSN hace referencia al destino de una activación remota. Especifique un RSN durante la instalación de una aplicación exportable de cliente en un equipo cliente. El procedimiento de instalación usa el RSN para dirigir la activación a un equipo cliente especificado. Para obtener más información sobre los nombres de cola, consulte la tabla de parámetros de la sección "Parámetros de Moniker de cola" de [Uso del Moniker de cola](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para especificar una aplicación COM+ como en cola, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Haga clic con el botón derecho en la aplicación para la que desea crear una cola y, a continuación, haga clic en **Propiedades.**

3.  Seleccione la **pestaña Cola en** el cuadro de diálogo de propiedades.

4.  Active la casilla con la etiqueta Queued : las colas de **MSMQ** pueden acceder a esta aplicación.

    > [!Note]  
    > Si la **casilla En** cola está atenuada, la aplicación no contiene componentes que se pueden poner en cola.

     

5.  Haga clic en **Aceptar**.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="remarks"></a>Comentarios

Las colas creadas por la biblioteca de administración de COM+ o la herramienta administrativa Servicios de componentes se marcan con el atributo transaccional de Message Queuing.

Una vez instalada una aplicación en cola en el servidor, se puede poner a disposición de los clientes mediante la exportación de la aplicación y, a continuación, la importación de la aplicación en cada cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de componentes que se pueden crear](creating-queuable-components.md)
</dt> <dt>

[Arquitectura de componentes en cola](queued-components-architecture.md)
</dt> </dl>

 

 



