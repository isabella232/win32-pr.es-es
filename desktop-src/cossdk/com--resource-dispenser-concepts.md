---
description: Los componentes de aplicación usan el dispensador de recursos de COM+ para tener acceso y administrar información de estado compartida y no duradera, como conexiones entre componentes y un administrador de recursos determinado.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Conceptos del dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807201"
---
# <a name="com-resource-dispenser-concepts"></a>Conceptos del dispensador de recursos COM+

Los componentes de aplicación usan el dispensador de recursos de COM+ para tener acceso y administrar información de estado compartida y no duradera, como conexiones entre componentes y un administrador de recursos determinado. En tiempo de ejecución, los grupos dinámicos de recursos, como las conexiones de base de datos, las conexiones de red, las conexiones a las colas, los subprocesos, los objetos y los bloques de memoria, se ponen a disposición del dispensador de recursos. El proceso de aplicación consigue un alto rendimiento mediante el uso de un número mínimo de recursos usados con frecuencia. El dispensador de recursos también puede automatizar las transacciones y la recuperación. (Consulte [recuperación automática de recursos](automatic-resource-reclamation.md) para obtener más información acerca de esta característica).

> [!Note]  
> Un *recurso* es todo lo que crea un dispensador de recursos. Por ejemplo, una conexión a un administrador de recursos es un recurso común. Los recursos residen en la memoria del dispensador de recursos y nunca se copian en el administrador dispensador. Un recurso solo lo conoce un identificador opaco (**Resid**) y puede o no ser capaz de realizar transacciones. Aunque los recursos administrados suelen ser conexiones a un componente que administra un estado duradero, las propias conexiones no son duraderas. Un dispensador de recursos suele usar un administrador de recursos relacionado para conservar el estado durable.

 

En la arquitectura, el sistema del dispensador de recursos COM+ está formado por distribuidores de recursos y un administrador dispensador. Los dispensadores de recursos son componentes proporcionados por el usuario que proporcionan a las aplicaciones interfaces simples para recursos compartidos. El gestor dispensador es un componente que proporciona COM+ y que coordina las actividades de los distintos distribuidores de recursos.

Un dispensador de recursos es un componente de biblioteca de vínculos dinámicos (DLL) que proporciona al menos dos interfaces. El primero, [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver), proporciona al administrador dispensador información básica sobre cómo crear, destruir y dar de alta los recursos que administra. La segunda se expone a las aplicaciones y puede ser una interfaz COM o un conjunto de interfaces o puede ser una interfaz de programación de aplicaciones (API) a la que se vincula un componente a través de una biblioteca de importación. Una aplicación puede llamar a cualquier dispensador de recursos, que a su vez puede ofrecer cualquier API a la aplicación. Si el dispensador de recursos es un componente de automatización, se puede tener acceso a él desde Microsoft Visual Basic. Se crea una instancia de un dispensador de recursos cuando un componente de aplicación hace referencia a él.

El administrador dispensador proporcionado por COM+ realiza un seguimiento de los distribuidores de recursos y las coordenadas entre ellos. Implementa dos interfaces: [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) y [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). los distribuidores de recursos se registran a sí mismos mediante la interfaz **IDispenserManager** . A continuación, el administrador dispensador les proporciona un puntero a un **IHolder** que usan para notificar a la Directora de sus actividades.

Un dispensador de recursos transaccionales debe darse de alta en una transacción Coordinador de transacciones distribuidas (DTC). Esto implica el uso de un administrador de recursos interno o externo (para el dispensador de recursos) que es compatible con las transacciones OLE.

> [!Note]  
> El modelo de programación COM+ incluye *transacciones declarativas*, que ayudan a proteger el trabajo realizado por un objeto de aplicación durante su duración. Cuando un objeto de aplicación utiliza un dispensador de recursos de COM+, el trabajo que realiza es automáticamente transaccional. es decir, el componente no tiene que declarar explícitamente las transacciones. Estas transacciones se definen en la especificación de transacciones OLE, implementadas por el DTC, y se inician en nombre del objeto de aplicación mediante COM+. Para obtener más información, consulte la guía de desarrollo de DTC.

 

Los recursos no deben ser transaccionales. Un dispensador de recursos que agrupe recursos no transaccionales todavía puede lograr un alto rendimiento al permitir que los objetos de aplicación tengan acceso a un grupo compartido de estos recursos. Este tipo de dispensador de recursos devuelve S \_ false del método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) , lo que significa que el dispensador de recursos no ha dado de alta el recurso porque el recurso no es transaccional.

El dispensador de recursos también puede funcionar independientemente de COM+, proporcionando únicamente capacidades de agrupación de recursos. Por ejemplo, si un dispensador de recursos expone una API (como ODBC), el dispensador de recursos podría ser un archivo DLL al que tenga acceso la aplicación a través de una biblioteca de importación (o mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ). Un dispensador de recursos también podría ser un componente COM al que tiene acceso una aplicación mediante una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Sin COM+, nunca se puede llamar al método [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) de un dispensador de recursos, ya que el administrador dispensador no tiene conocimiento de la transacción del componente actual.

Al iniciarse, un archivo DLL de dispensador de recursos debe registrarse en el administrador del dispensador. El gestor dispensador es el ejecutivo de control que administra la carga y descarga de los distribuidores de recursos, proporciona el contexto de COM+ y controla el administrador de estadísticas de inventario. (Para obtener más información, consulte [Administrador de dispensadores de com+](com--dispenser-manager.md)). El dispensador de recursos llama primero a la función [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) y, a continuación, llama al método [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) , pasando el puntero [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) que implementa el dispensador de recursos. Esta llamada devuelve una referencia a [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder).

Para apagarse, un dispensador de recursos llama a [**IHolder:: Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close). Para garantizar un cierre de un paquete limpio, un dispensador de recursos debe ser capaz de controlar la situación en la que las llamadas continúan llegando desde objetos empresariales después de que COM+ haya solicitado el cierre del dispensador.

En los siguientes temas de esta sección se proporciona información más detallada sobre el servicio dispensador de recursos COM+:

-   [Administrador del dispensador de COM+](com--dispenser-manager.md)
-   [Tipos de subprocesos del dispensador de recursos COM+](com--resource-dispenser-thread-types.md)
-   [Estados de recursos agrupados disponibles para el dispensador de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Dar de alta un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
-   [Proceso de asignación de recursos del dispensador de recursos](resource-dispenser-resource-allocation-process.md)
-   [Seguimiento de recursos no asignados](tracking-non-allocated-resources.md)
-   [Recuperación automática de recursos](automatic-resource-reclamation.md)
-   [Tipos usados en las interfaces del dispensador de recursos COM+](types-used-in-com--resource-dispenser-interfaces.md)
-   [Interfaces dispensadoras de recursos COM+](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas del dispensador de recursos COM+](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
