---
description: Implementación para una comunicación más rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implementación para una comunicación más rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264527"
---
# <a name="deploying-for-faster-communication"></a>Implementación para una comunicación más rápida

El rendimiento es una consideración clave al implementar una aplicación COM+, y la ubicación del componente es la clave para obtener el mejor rendimiento de una aplicación bien diseñada.

Una vez se ha mantenido ampliamente que, con las arquitecturas de aplicaciones escalables, el rendimiento podría abordarse simplemente moviendo los componentes principales de la aplicación a un hardware más rápido. Esto ha demostrado no ser cierto. Los problemas de rendimiento no surgen del rendimiento de componentes individuales, sino de los vínculos que conectan los componentes.

El factor principal para el éxito es la ubicación. Proximidad o ubicación física, tiempo, capacidad y propósito son distintos aspectos de la ubicación que se aplican a la implementación de una aplicación COM+, que afectan al rendimiento.

El mejor rendimiento se produce cuando los componentes y recursos de la aplicación se diseñan e implementan para satisfacer las demandas que les exige la carga de trabajo de la aplicación.

En general, debe implementar componentes para minimizar la comunicación entre procesos y, especialmente, entre equipos entre componentes. Si el diseño de la aplicación es eficaz, las clases dentro de un componente se agrupan por uso y función para maximizar las comunicaciones dentro de los componentes. Al implementar componentes, debe asegurarse de que los componentes se encuentran lógicamente para hacer uso de las relaciones entre los componentes y reducir la cantidad de mensajería entre los componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> </dl>

 

 



