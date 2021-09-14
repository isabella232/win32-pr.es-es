---
description: Los componentes de la aplicación usan el dispensador de recursos COM+ para acceder a la información de estado compartida y no duradera, como las conexiones entre componentes y un administrador de recursos determinado.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Conceptos del distribuidor de recursos com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973537"
---
# <a name="com-resource-dispenser-concepts"></a>Conceptos del distribuidor de recursos com+

Los componentes de la aplicación usan el dispensador de recursos COM+ para acceder a la información de estado compartida y no duradera, como las conexiones entre componentes y un administrador de recursos determinado. En tiempo de ejecución, los grupos dinámicos de recursos, como las conexiones de base de datos, las conexiones de red, las conexiones a colas, subprocesos, objetos y bloques de memoria, están disponibles para el distribuidor de recursos. El proceso de aplicación logra un alto rendimiento mediante el uso de un número mínimo de recursos usados con frecuencia. El distribuidor de recursos también puede automatizar las transacciones y la reclamación. (Consulte [Recuperación automática de recursos](automatic-resource-reclamation.md) para obtener más información sobre esta característica).

> [!Note]  
> Un *recurso* es todo lo que crea un dispensador de recursos. Por ejemplo, una conexión a un administrador de recursos es un recurso común. Los recursos residen en la memoria del distribuidor de recursos y nunca se copian en el administrador del dispensador. Un recurso solo lo conoce un identificador opaco **(RESID)** y puede o no ser capaz de realizar transacciones. Aunque los recursos administrados a menudo pueden ser conexiones a un componente que administra un estado duradero, las propias conexiones no son duraderas. A menudo, un dispensador de recursos usa un administrador de recursos relacionado para conservar el estado duradero.

 

En la arquitectura, el sistema de dispensador de recursos COM+ consta de dispensadores de recursos y un administrador de dispensadores. Los distribuidores de recursos son componentes proporcionados por el usuario que proporcionan a las aplicaciones interfaces sencillas para los recursos compartidos. El administrador de dispensadores es un componente proporcionado por COM+ que coordina las actividades de los distintos distribuidores de recursos.

Un dispensador de recursos es un componente de biblioteca de vínculos dinámicos (DLL) que proporciona al menos dos interfaces. El primero, [**IDispenserDriver,**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)proporciona al administrador de distribuidores información básica sobre cómo crear, destruir y dar de alta los recursos que administra. El segundo se expone a las aplicaciones y puede ser una interfaz COM o un conjunto de interfaces o puede ser una interfaz de programación de aplicaciones (API) a la que un componente está vinculado a través de una biblioteca de importación. Una aplicación puede llamar a cualquier distribuidor de recursos, que a su vez puede ofrecer cualquier API a la aplicación. Si el distribuidor de recursos es un componente de Automation, se puede acceder a él desde Microsoft Visual Basic. Se crea una instancia de un dispensador de recursos cuando un componente de aplicación hace referencia a él.

El administrador de dispensador proporcionado por COM+ realiza un seguimiento de los dispensadores de recursos y las coordenadas entre ellos. Implementa dos interfaces: [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) e [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). Los distribuidores de recursos se registran mediante la **interfaz IDispenserManager.** A continuación, el administrador de dispensadores les proporciona un puntero a **un IHolder** que usan para notificar al administrador de dispensadores sus actividades.

Un dispensador de recursos transaccional debe dar de alta en una transacción Coordinador de transacciones distribuidas (DTC). Esto implica el uso de un administrador de recursos interno o externo (al distribuidor de recursos) que sea compatible con transacciones OLE.

> [!Note]  
> El modelo de programación COM+ *incluye transacciones declarativas,* que ayudan a proteger el trabajo realizado por un objeto de aplicación durante su vigencia. Cuando un objeto de aplicación usa un dispensador de recursos COM+, el trabajo que realiza es transaccional automáticamente. Es decir, el componente no tiene que declarar transacciones explícitamente. Estas transacciones se definen en la especificación de transacciones OLE, implementadas por DTC e iniciadas en nombre del objeto de aplicación por COM+. Consulte la Guía de desarrollo de DTC para obtener más información.

 

Los recursos no deben ser transaccionales. Un dispensador de recursos que agrupa recursos no transaccionales todavía puede lograr un alto rendimiento al permitir que los objetos de aplicación accedan a un grupo compartido de estos recursos. Este tipo de dispensador de recursos devuelve S FALSE desde el método \_ [**IDispenserDriver::EnlistResource,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) lo que significa que el distribuidor de recursos no dio de alta el recurso porque el recurso no es transaccional.

El dispensador de recursos también puede funcionar independientemente de COM+, lo que proporciona solo funcionalidades de agrupación de recursos. Por ejemplo, si un dispensador de recursos expone una API (como ODBC), el dispensador de recursos podría ser un archivo DLL al que la aplicación tiene acceso a través de una biblioteca de importación (o mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress).**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) Un dispensador de recursos también podría ser un componente COM al que una aplicación tiene acceso mediante una llamada [**a CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Sin COM+, nunca se puede llamar al método [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) de un distribuidor de recursos porque el administrador del distribuidor no tiene conocimiento de la transacción del componente actual.

Al iniciarse, un archivo DLL de dispensador de recursos debe registrarse en el administrador del dispensador. El administrador de dispensadores es el ejecutivo de control que administra la carga y descarga de los distribuidores de recursos, proporciona el contexto COM+ y controla el administrador de estadísticas de inventario. (Para obtener más información, [vea Com+ Dispenser Manager).](com--dispenser-manager.md) El dispensador de recursos llama primero a la función [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) y, después, llama al método [**IDispenserManager::RegisterDispenser,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) pasando el puntero [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) que implementa el distribuidor de recursos. Esta llamada devuelve una referencia a [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder).

Para cerrar, un dispensador de recursos llama a [**IHolder::Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close). Para garantizar el apagado de un paquete limpio, un distribuidor de recursos debe ser capaz de controlar la situación en la que las llamadas siguen llegando desde objetos empresariales después de que COM+ haya pedido al distribuidor que se apague.

Los temas siguientes de esta sección proporcionan información más detallada sobre el servicio de dispensador de recursos COM+:

-   [Administrador de dispensadores COM+](com--dispenser-manager.md)
-   [Tipos de subprocesos de dispensador de recursos COM+](com--resource-dispenser-thread-types.md)
-   [Estados de recursos agrupados disponibles para el distribuidor de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Registro de un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
-   [Proceso de asignación de recursos del distribuidor de recursos](resource-dispenser-resource-allocation-process.md)
-   [Seguimiento de recursos no asignados](tracking-non-allocated-resources.md)
-   [Recuperación automática de recursos](automatic-resource-reclamation.md)
-   [Tipos usados en interfaces de dispensador de recursos com+](types-used-in-com--resource-dispenser-interfaces.md)
-   [Interfaces de dispensador de recursos COM+](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas del distribuidor de recursos com+](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
