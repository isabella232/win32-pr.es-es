---
description: Algunas aplicaciones están diseñadas de forma que evita que se instalen varias instancias de la aplicación en un equipo.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restricciones de diseño de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686436"
---
# <a name="application-design-restrictions"></a>Restricciones de diseño de aplicaciones

Algunas aplicaciones están diseñadas de forma que evita que se instalen varias instancias de la aplicación en un equipo. Con este tipo de limitación, una aplicación no puede usar la característica de particiones. Es posible que sea necesario modificar las siguientes características de diseño de aplicaciones antes de que se puedan usar particiones para esa aplicación.

## <a name="tables-and-arrays"></a>Tablas y matrices

Algunas aplicaciones crean tablas de base de datos, tablas en memoria o matrices que usan un CLSID como clave de registro única. En un equipo sin particiones, esta clave del registro suele ser Computer/CLSID (un CLSID por equipo).

Por el contrario, en un equipo con particiones, esta clave del registro es el identificador de equipo/partición/ID. de aplicación/CLSID (varias instancias de un CLSID por equipo). Dado que la característica particiones permite que existan varias instancias de un CLSID en un equipo, las aplicaciones que contienen elementos de diseño que requieren un CLSID único por equipo podrían verse afectadas negativamente.

## <a name="global-resources"></a>Recursos globales

Algunas aplicaciones usan recursos globales como memoria compartida, archivos de datos y entradas del registro. Esto podría causar problemas si se ejecutan varias instancias de este tipo de aplicación simultáneamente.

Por ejemplo, si un componente utiliza memoria compartida para interactuar con otros componentes, deberá modificar el componente para que cada instancia del componente asigne su propia memoria compartida.

## <a name="type-libraries"></a>Bibliotecas de tipos

Las bibliotecas de tipos proporcionan información sobre las interfaces y los métodos de un componente. Esta información se usa para varios propósitos, entre los que se incluyen los siguientes:

-   Serialización de datos entre componentes cuando se realizan llamadas de función
-   Ayuda de los componentes en cola de COM+ y los servicios de eventos COM+
-   Proporcionar la información correcta en un editor de Microsoft Visual Basic

Las referencias a una biblioteca de tipos se instalan en el registro de un equipo. Al desarrollar aplicaciones que se invocarán desde particiones, es importante que se instale la versión más reciente de una biblioteca de tipos en el registro. Esto garantiza que el editor de Visual Basic que se utiliza obtendrá información precisa sobre los métodos disponibles para ese componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones y componentes en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



