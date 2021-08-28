---
description: COM+ proporciona un entorno de desarrollo empresarial, basado en el Modelo de objetos componentes (COM) de Microsoft, para crear aplicaciones distribuidas basadas en componentes.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Introducción a la programación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421fd6a52eade351eaab09ececff8fc63cc687002dede350ab9f06fa0b2c20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096895"
---
# <a name="com-programming-overview"></a>Introducción a la programación de COM+

COM+ proporciona un entorno de desarrollo empresarial, basado en el Modelo de objetos componentes (COM) de Microsoft, para crear aplicaciones distribuidas basadas en componentes. También proporciona las herramientas para crear aplicaciones transaccionales de varios niveles. COM+ combina mejoras en el desarrollo tradicional basado en COM con muchos servicios administrativos y de programación útiles. Consulte [Servicios COM+](com--services.md) para obtener una lista completa de estos servicios.

Las mejoras com incluyen mejoras en el subprocesamiento y la seguridad, junto con la introducción de los servicios de sincronización. Los servicios incluyen la herramienta administrativa Servicios de componentes.

Para aquellos familiarizados con la programación COM, las mejoras de COM+ son significativas, incluidas las siguientes:

-   COM+ implementa un modelo de subprocesamiento denominado subprocesamiento de apartamento neutro, que permite a un componente tener acceso serializado junto con la capacidad de ejecutarse en cualquier subproceso.
-   COM+ admite componentes con un entorno especial denominado [contexto](com--contexts.md), que proporciona un conjunto extensible de propiedades que definen el entorno de ejecución para el componente.
-   COM+ proporciona seguridad basada en roles, ejecución asincrónica de objetos y un moniker integrado que representa una referencia a una instancia de objeto que se ejecuta en un servidor fuera de proceso.

## <a name="application-and-component-administration"></a>Administración de aplicaciones y componentes

En COM+, una base de datos de registro, denominada RegDB, almacena los metadatos que describen los componentes. Esta base de datos está muy optimizada para el tipo de información que COM+ necesita para la activación de componentes y se usa en lugar del registro del sistema. Además, COM+ expone el catálogo *de COM+,* que tiene acceso a la información de RegDB. El catálogo de COM+ es un almacén de datos del sistema que contiene información de configuración para aplicaciones COM+ en un equipo servidor determinado.

Por último, la herramienta administrativa Servicios de componentes proporciona una interfaz de usuario totalmente compatible con scripts para que los desarrolladores y administradores administren componentes, así como para implementar aplicaciones de varios nivel del lado cliente y del lado servidor. Para obtener más información, vea [Implementación de aplicaciones COM+.](deploying-com--applications.md)

## <a name="automatic-transactions"></a>Transacciones automáticas

COM+ admite toda la semántica de Microsoft Transaction Server (MTS) 2.0 y agrega la funcionalidad [auto-done,](enabling-auto-done-for-a-method.md) que puede establecer mediante la herramienta administrativa Servicios de componentes. Esta característica permite al sistema anular automáticamente una transacción si se desencadena una excepción o confirmar si no es así. Para obtener más información, [vea Transacciones COM+](com--transactions.md)y [Activación Just-In-Time de COM+.](com--just-in-time-activation.md)

 

 



