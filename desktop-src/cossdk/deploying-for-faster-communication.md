---
description: Implementación para una comunicación más rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implementación para una comunicación más rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201185878a6d3fc041512b41fd3f51975ae5e0988f853dbbbcb77b716ea4cebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070785"
---
# <a name="deploying-for-faster-communication"></a>Implementación para una comunicación más rápida

El rendimiento es una consideración clave al implementar una aplicación COM+, y la ubicación del componente es la clave para obtener el mejor rendimiento de una aplicación bien diseñada.

Una vez se ha mantenido ampliamente que, con las arquitecturas de aplicaciones escalables, el rendimiento se podía abordar simplemente moviendo los componentes principales de la aplicación a hardware más rápido. Esto ha demostrado que no es cierto. Los problemas de rendimiento no surgen del rendimiento de componentes individuales, sino de los vínculos que conectan los componentes.

El factor principal para el éxito es la ubicación. Proximidad o ubicación física, tiempo, capacidad y propósito son aspectos distintos de la ubicación que se aplican a la implementación de una aplicación COM+, que afectan al rendimiento.

El mejor rendimiento se produce cuando los componentes y recursos de la aplicación se diseñan e implementan para satisfacer las demandas que les exige la carga de trabajo de la aplicación.

En general, debe implementar componentes para minimizar la comunicación entre procesos y, especialmente, entre equipos entre componentes. Si el diseño de la aplicación es eficaz, las clases dentro de un componente se agrupan por uso y función para maximizar las comunicaciones dentro de los componentes. En la implementación de componentes, debe asegurarse de que los componentes se encuentran lógicamente para hacer uso de las relaciones entre los componentes y reducir la cantidad de mensajería entre componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> </dl>

 

 



