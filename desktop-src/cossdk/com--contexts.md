---
description: En el caso de los componentes configurados que se ejecutan en aplicaciones COM+, los contextos son la base en la que se proporcionan los servicios COM+.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contextos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0ae1228f89797f9124e817db07f11a23dbec12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973545"
---
# <a name="com-contexts"></a>Contextos COM+

En el caso de los componentes configurados que se ejecutan en aplicaciones COM+, los *contextos* son la base en la que se proporcionan los servicios COM+. En COM+, un contexto se define como un conjunto de propiedades en tiempo de ejecución asociadas a uno o varios objetos COM que se usan para proporcionar servicios para esos objetos.

En COM+, cada objeto COM se asocia exactamente a un contexto mientras se ejecuta (es decir, entre su activación y desactivación) y cada contexto reside exactamente dentro de un apartamento COM. Se pueden ejecutar varios objetos en el mismo contexto y varios contextos pueden residir en el mismo apartamento. Inicializadas cuando se activa un objeto, las propiedades de contexto, como las propiedades de contexto de seguridad, representan las necesidades en tiempo de ejecución de un objeto.

> [!Note]  
> En el caso de los componentes no configurados que no usan servicios COM+, el contexto se omite en su mayor parte.

 

COM+ usa las propiedades de contexto como base para proporcionar servicios en tiempo de ejecución. Estas propiedades mantienen el estado que determina cómo el entorno de ejecución realiza servicios para los objetos dentro del contexto. En algunos casos, puede interactuar directamente con las propiedades de contexto de un objeto para indicar algún estado relevante para un servicio que se proporciona para el objeto. Por ejemplo, lo haría cuando un objeto que participa en una transacción automática vote sobre el resultado de la transacción.

Para obtener una explicación detallada de la base COM de estos conceptos, vea [Procesos, subprocesos y alojamientos](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Interacción mediante programación con propiedades de contexto

Cada contexto tiene un objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) asociado que realiza un seguimiento de sus propiedades. Puede acceder a **ObjectContext llamando** a la [**función GetObjectContext.**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) Una vez que haya accedido a **ObjectContext,** puede llamar a métodos en la [**interfaz IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) que expone para manipular las propiedades de contexto.

Por ejemplo, llamar a [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) tiene el efecto de establecer el bit de coherencia de transacción en "coherente" y el bit [JIT-activation](com--just-in-time-activation.md) done en "done" en el contexto asociado al objeto . "Coherente" indica a COM+ que vote por confirmar la transacción y "listo" indica que el objeto está listo para desactivarse cuando el método vuelva.

Además de [**IObjectContext, otras**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)interfaces especializadas que proporcionan acceso a las propiedades de contexto son [**IObjectContextInfo,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo) [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)y [**IObjectContextActivity.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity) Hasta cierto punto, [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) también tiene acceso a las propiedades de contexto. Puede usar [**IGetSecurityCallContext::GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obtener **ISecurityCallContext.**

## <a name="understanding-activation-and-interception"></a>Descripción de la activación y la intercepción

Por lo general, solo debe pensar en el contexto en la medida en que representa una serie de propiedades, algunas de las cuales puede establecer u obtener, que se usan para proporcionar servicios COM+ para los componentes. Sin embargo, en algunas circunstancias, es posible que deba tener en cuenta las dos facetas de contextos interrelacionadas siguientes con más detalle:

-   [Activación de contexto](context-activation.md)o inicialización de un objeto en un contexto adecuado.
-   [Interceptación](interception-of-cross-context-calls.md), o lo que hace COM+ en las llamadas a través de un límite de contexto.

## <a name="relation-to-mts-context-wrappers"></a>Relación con los contenedores de contexto de MTS

Los contextos reemplazan eficazmente los contenedores de contexto de MTS. El propósito que sirven, proporcionar servicios automáticos mediante la captura de solicitudes de creación, es ahora una característica integrada de COM+. Como resultado, ya no es necesario usar la [**función SafeRef.**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) En MTS, **SafeRef** se usó para obtener una referencia al objeto que se podría pasar fuera de su contenedor de contexto. En COM+, esto no es necesario; las referencias a objetos **normales** (estos punteros) funcionan.

 

 
