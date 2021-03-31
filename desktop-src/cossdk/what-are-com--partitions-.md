---
description: Una partición COM+ es un contenedor lógico que permite a las aplicaciones ejecutarse independientemente de otras configuraciones de esas aplicaciones.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: ¿Qué son las particiones COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104156972"
---
# <a name="what-are-com-partitions"></a>¿Qué son las particiones COM+?

Una partición COM+ es un contenedor lógico que permite a las aplicaciones ejecutarse independientemente de otras configuraciones de esas aplicaciones. Cada configuración de una aplicación se instala en una partición independiente y se puede administrar por separado, de acuerdo con las necesidades específicas de los usuarios.

Durante la activación de un componente COM+, el servicio particiones determina la configuración del componente que se va a activar, en función de la identidad del usuario que solicita la activación del componente. Por ejemplo, una sola organización que tiene dos grupos independientes, producción y entrenamiento, podría implementar particiones COM+ como una manera de permitir que los dos grupos usen configuraciones diferentes de una aplicación COM+ en el mismo equipo.

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición de COM+ disponible.

**Windows 2000:** El servicio de particiones COM+ no está disponible en Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Ventajas del uso de particiones COM+

El uso de particiones COM+ ofrece varias ventajas, entre las que se incluyen las siguientes:

-   Las organizaciones pueden reducir el costo total de propiedad (TCO) mediante el uso de menos servidores de aplicaciones físicos para admitir usuarios que necesitan varias configuraciones de aplicaciones.
-   Se reduce la sobrecarga administrativa. En lugar de tener que configurar y administrar varios equipos, los administradores solo necesitan configurar y administrar varias particiones en el mismo equipo. Además, las particiones se pueden administrar mediante programación a través de la adición de una nueva interfaz de programación de COM+.
-   La seguridad se puede implementar y administrar partición a partición para usuarios locales, usuarios del dominio y unidades organizativas (OU).
-   Los programadores y administradores pueden utilizar las herramientas administrativas y de desarrollo de Microsoft, como el Windows SDK, Active Directory usuarios y equipos, y la herramienta administrativa Servicios de componentes, para administrar particiones COM+. La característica de particiones está totalmente integrada en estas herramientas.

## <a name="primary-usage-scenario"></a>Escenario de uso principal

Una razón principal para que los clientes implementen la característica de particiones de COM+ es hospedar aplicaciones basadas en Web. Por ejemplo, supongamos que una pequeña compañía de software desarrolla una aplicación COM+ para su uso por parte del personal del hospital. La aplicación, que es una aplicación distribuida basada en Web, proporciona una manera para que los hospitales almacenen y recuperen registros médicos de pacientes mediante una base de datos de SQL Server.

Supongamos que la compañía de software tiene tres clientes: Hospital A, hospital B y Hospital C. Aunque cada cliente ejecuta el lado cliente de la aplicación COM+ localmente en sus equipos de escritorio, el lado servidor de la aplicación COM+ reside en el servidor Web interno de la empresa de software y es accesible por sus clientes a través de la Web.

Dado que cada hospital tiene su propio conjunto de requisitos de almacenamiento y recuperación y su propio conjunto de datos de pacientes personalizados, la compañía de software debe proporcionar una manera de que varias configuraciones de la parte del servidor de la aplicación se ejecuten simultáneamente en el servidor Web. Las particiones COM+ proporcionan una solución a este problema.

En la siguiente ilustración se muestra el escenario de particiones de la aplicación COM+ de la compañía de software.

![Diagrama que muestra un escenario de particiones para una aplicación COM+, con una aplicación cliente para la aplicación de servidor en la base de datos de SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Particiones y componentes en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



