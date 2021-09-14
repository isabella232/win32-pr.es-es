---
description: Una partición COM+ es un contenedor lógico que permite que las aplicaciones se ejecuten independientemente de otras configuraciones de esas aplicaciones.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: ¿Qué son las particiones COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973488"
---
# <a name="what-are-com-partitions"></a>¿Qué son las particiones COM+?

Una partición COM+ es un contenedor lógico que permite que las aplicaciones se ejecuten independientemente de otras configuraciones de esas aplicaciones. Cada configuración de una aplicación se instala en una partición independiente y se puede administrar por separado, según las necesidades específicas de sus usuarios.

Durante la activación de un componente COM+, el servicio de particiones determina qué configuración del componente se va a activar, en función de la identidad del usuario que solicita la activación del componente. Por ejemplo, una sola organización que tenga dos grupos independientes, Producción y Entrenamiento, podría implementar particiones COM+ como una manera de permitir que los dos grupos usen configuraciones diferentes de una aplicación COM+ en el mismo equipo.

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición com+ disponible.

**Windows 2000:** El servicio de particiones COM+ no está disponible en Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Ventajas del uso de particiones COM+

El uso de particiones COM+ ofrece varias ventajas, entre las que se incluyen las siguientes:

-   Las organizaciones pueden reducir su costo total de propiedad (TCO) mediante el uso de menos servidores de aplicaciones físicos para admitir usuarios que necesitan varias configuraciones de aplicación.
-   Se reduce la sobrecarga administrativa. En lugar de tener que configurar y administrar varios equipos, los administradores solo necesitan configurar y administrar varias particiones en el mismo equipo. Además, las particiones se pueden administrar mediante programación mediante la adición de una nueva interfaz de programación COM+.
-   La seguridad se puede implementar y administrar en función de la partición para usuarios locales, usuarios de dominio y unidades organizativas (UO).
-   Los programadores y administradores pueden usar las herramientas administrativas y de desarrollo de Microsoft, como el SDK de Windows, Usuarios y equipos de Active Directory y la herramienta administrativa servicios de componentes, para administrar particiones com+. La característica de particiones está totalmente integrada en estas herramientas.

## <a name="primary-usage-scenario"></a>Escenario de uso principal

Una razón principal para que los clientes implemente la característica de particiones COM+ es hospedar aplicaciones basadas en web. Por ejemplo, suponga que una pequeña empresa de software desarrolla una aplicación COM+ para que la use el personal del hospital. La aplicación, que es una aplicación distribuida basada en Web, proporciona una manera de que los hospitales almacenen y recuperen los registros médicos de los pacientes mediante una base SQL Server datos.

Supongamos que la empresa de software tiene tres clientes: Hospital A, Hospital B y Hospital C. Mientras que cada cliente ejecuta el lado cliente de la aplicación COM+ localmente en sus equipos de escritorio, el lado servidor de la aplicación COM+ reside en el servidor web local de la empresa de software y sus clientes acceden a ellos a través de la Web.

Dado que cada hospital tiene su propio conjunto de requisitos de almacenamiento y recuperación y su propio conjunto de datos de pacientes personalizados, la empresa de software debe proporcionar una manera de que varias configuraciones de la parte del servidor de la aplicación se ejecuten simultáneamente en el servidor web. Las particiones COM+ proporcionan una solución a este problema.

En la ilustración siguiente se muestra el escenario de particiones para la aplicación COM+ de la empresa de software.

![Diagrama que muestra un escenario de particiones para una aplicación COM+, con una aplicación cliente a una aplicación de servidor a la base de datos SQL servidor.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Componentes y particiones en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



