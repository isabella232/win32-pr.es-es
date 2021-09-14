---
description: Algunas aplicaciones están diseñadas de forma que impide que varias instancias de la aplicación se instalen en un equipo.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restricciones de diseño de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073022"
---
# <a name="application-design-restrictions"></a>Restricciones de diseño de aplicaciones

Algunas aplicaciones están diseñadas de forma que impide que varias instancias de la aplicación se instalen en un equipo. Con esta limitación, una aplicación no puede hacer uso de la característica de particiones. Es posible que sea necesario modificar las siguientes características de diseño de aplicaciones para poder usar particiones para esa aplicación.

## <a name="tables-and-arrays"></a>Tablas y matrices

Algunas aplicaciones crean tablas de base de datos, tablas en memoria o matrices que usan un CLSID como clave del Registro única. En un equipo sin particiones, esta clave del Registro suele ser equipo/CLSID (un CLSID por equipo).

Por el contrario, en un equipo con particiones, esta clave del Registro es computer/partition ID/application ID/CLSID (varias instancias de un CLSID por equipo). Dado que la característica de particiones permite que existan varias instancias de un CLSID en un equipo, las aplicaciones que contienen elementos de diseño que requieren un CLSID único por equipo podrían verse afectadas negativamente.

## <a name="global-resources"></a>Recursos globales

Algunas aplicaciones usan recursos globales, como memoria compartida, archivos de datos y entradas del Registro. Esto podría causar problemas si varias instancias de este tipo de aplicación se ejecutan simultáneamente.

Por ejemplo, si un componente usa memoria compartida para interactuar con otros componentes, el componente deberá modificarse para que cada instancia del componente asigne su propia memoria compartida.

## <a name="type-libraries"></a>Bibliotecas de tipos

Las bibliotecas de tipos proporcionan información sobre las interfaces y los métodos de un componente. Esta información se usa para varios propósitos, incluidos los siguientes:

-   Serialización de datos entre componentes cuando se realizan llamadas de función
-   Ayuda a los componentes en cola de COM+ y a los servicios de eventos COM+
-   Proporcionar la información correcta dentro de un editor de Visual Basic Microsoft

Las referencias a una biblioteca de tipos se instalan en el Registro de un equipo. Al desarrollar aplicaciones que se invocarán desde particiones, es importante que la versión más reciente de una biblioteca de tipos esté instalada en el Registro. Esto garantiza que el editor Visual Basic que se está utilizando obtenga información precisa sobre los métodos disponibles para ese componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes y particiones en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de partición](partition-implementation.md)
</dt> <dt>

[Registro y activación de componentes en particiones](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



