---
description: Implementación para una comunicación más rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implementación para una comunicación más rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677244"
---
# <a name="deploying-for-faster-communication"></a>Implementación para una comunicación más rápida

El rendimiento es una consideración importante a la hora de implementar una aplicación COM+ y la ubicación del componente es la clave para obtener el mejor rendimiento de una aplicación bien diseñada.

Una vez que se mantuvo con arquitecturas de aplicaciones escalables, el rendimiento se podía solucionar simplemente moviendo los componentes principales de la aplicación a un hardware más rápido. Esto ha demostrado que no es cierto. Los problemas de rendimiento no se producen desde el rendimiento de los componentes individuales, sino desde los vínculos que conectan los componentes.

El factor principal para el éxito es la ubicación. La ubicación física o la proximidad, la hora, la capacidad y el propósito son distintos aspectos de la ubicación que se aplican a la implementación de una aplicación COM+, lo que afecta al rendimiento.

El mejor rendimiento se produce cuando se diseñan e implementan los componentes y los recursos de la aplicación para que coincidan con las demandas aplicadas por la carga de trabajo de la aplicación.

En general, debe implementar los componentes para minimizar la comunicación entre los componentes y el proceso entre los distintos procesos. Si el diseño de la aplicación es eficaz, las clases de un componente se agrupan por uso y función para maximizar las comunicaciones dentro de los componentes. En la implementación de componentes, debe asegurarse de que los componentes están ubicados lógicamente para hacer uso de las relaciones entre los componentes y reducir la cantidad de mensajería entre los componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar para la implementación](designing-for-deployment.md)
</dt> </dl>

 

 



