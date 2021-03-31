---
description: COM+ proporciona un entorno de desarrollo empresarial, basado en el modelo de objetos componentes (COM) de Microsoft, para crear aplicaciones distribuidas basadas en componentes.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Información general sobre programación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c225b5ebb6f04f74d6071dc0305d219993fa606e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807207"
---
# <a name="com-programming-overview"></a>Información general sobre programación de COM+

COM+ proporciona un entorno de desarrollo empresarial, basado en el modelo de objetos componentes (COM) de Microsoft, para crear aplicaciones distribuidas basadas en componentes. También proporciona las herramientas para crear aplicaciones transaccionales de varios niveles. COM+ combina mejoras en el desarrollo tradicional basado en COM con muchos servicios de programación y administrativos útiles. Vea [servicios com+](com--services.md) para obtener una lista completa de estos servicios.

Las mejoras de COM incluyen mejoras en los subprocesos y la seguridad, junto con la introducción de los servicios de sincronización. Los servicios incluyen la herramienta administrativa Servicios de componentes.

Para aquellos que estén familiarizados con la programación COM, las mejoras de COM+ son significativas, entre las que se incluyen las siguientes:

-   COM+ implementa un modelo de subprocesos denominado subprocesamiento de Apartamento neutro, que permite que un componente tenga acceso serializado junto con la capacidad de ejecutarse en cualquier subproceso.
-   COM+ admite componentes con un entorno especial denominado [contexto](com--contexts.md), que proporciona un conjunto extensible de propiedades que definen el entorno de ejecución del componente.
-   COM+ proporciona seguridad basada en roles, ejecución asincrónica de objetos y un moniker integrado que representa una referencia a una instancia de objeto que se ejecuta en un servidor fuera de proceso.

## <a name="application-and-component-administration"></a>Administración de aplicaciones y componentes

En COM+, una base de datos de registro, denominada RegDB, almacena los metadatos que describen los componentes. Esta base de datos está muy optimizada para el tipo de información que COM+ necesita para la activación de componentes y se usa en lugar del registro del sistema. Además, COM+ expone el *Catálogo com+*, que obtiene acceso a la información de RegDB. El catálogo de COM+ es un almacén de datos del sistema que contiene información de configuración para las aplicaciones COM+ en un equipo servidor determinado.

Por último, la herramienta administrativa Servicios de componentes proporciona una interfaz de usuario totalmente Scriptable para que los desarrolladores y administradores administren componentes, así como para implementar aplicaciones de varios niveles en el cliente y en el lado servidor. Para obtener más información, consulte [DEPLOYING com+ Applications](deploying-com--applications.md).

## <a name="automatic-transactions"></a>Transacciones automáticas

COM+ es compatible con toda la semántica de Microsoft Transaction Server (MTS) 2,0 y agrega la funcionalidad [de realización automática](enabling-auto-done-for-a-method.md) , que se puede establecer mediante la herramienta administrativa Servicios de componentes. Esta característica permite al sistema anular automáticamente una transacción si se desencadena una excepción o confirmar si no es así. Para obtener más información, vea [transacciones com+](com--transactions.md)y [activación Just-in-Time de com+](com--just-in-time-activation.md).

 

 



