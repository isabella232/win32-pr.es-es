---
description: Servicios COM+ sin componentes
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servicios COM+ sin componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153208"
---
# <a name="com-services-without-components"></a>Servicios COM+ sin componentes

Con COM+ 1,5, puede usar los servicios proporcionados por COM+ sin necesidad de generar un componente que contenga los métodos que llaman a esos servicios. Esto beneficia a los desarrolladores que normalmente no usan componentes, sino que desean usar servicios COM+ como transacciones o el seguimiento de COM+. Mediante el uso de servicios COM+ sin componentes, los desarrolladores pueden evitar la sobrecarga que supone crear un componente que se usa para tener acceso únicamente a los servicios COM+ que necesitan.

Por ejemplo, los entornos de scripts solían ser los mayores consumidores de los servicios COM+, pero nunca podían usar esos servicios de forma eficaz, ya que los servicios debían estar integrados en un componente de COM+. Este requisito de agrupación aumentó los costos de rendimiento debido al aumento de la comunicación y la duplicación de los datos necesarios para que el entorno de scripting interactúe con el componente. Al usar servicios sin componentes, se minimizan los costos.

En los temas que se describen en la tabla siguiente se proporciona información básica y de tareas sobre el uso de servicios COM+ sin componentes. Esta característica está pensada para los programadores de Visual C++ avanzados que preocupan del rendimiento.



| Tema                                                                                                 | Descripción                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Conceptos de servicios COM+ sin componentes](com--services-without-components-concepts.md)<br/> | Proporciona información general sobre el uso de servicios COM+ sin componentes.<br/>                     |
| [Servicios COM+ sin tareas de componentes](com--services-without-components-tasks.md)<br/>       | Proporciona instrucciones para usar COM+ con el fin de crear y usar servicios sin componentes.<br/> |



 

 

 




