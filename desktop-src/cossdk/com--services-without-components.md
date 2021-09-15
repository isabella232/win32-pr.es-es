---
description: Servicios COM+ sin componentes
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servicios COM+ sin componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258615"
---
# <a name="com-services-without-components"></a>Servicios COM+ sin componentes

Con COM+ 1.5, puede usar los servicios proporcionados por COM+ sin necesidad de compilar un componente para contener los métodos que llaman a esos servicios. Esto beneficia en gran medida a los desarrolladores que no suelen usar componentes, pero quieren usar servicios COM+, como transacciones o el rastreador com+. Mediante el uso de servicios COM+ sin componentes, los desarrolladores pueden evitar la sobrecarga de crear un componente que se usa para acceder solo a los servicios COM+ que necesitan.

Por ejemplo, los entornos de script tradicionalmente han sido los mayores consumidores de servicios COM+, pero nunca pudieron usar esos servicios de forma eficaz porque los servicios tenían que agruparse dentro de un componente COM+. Este requisito de unión aumenta los costos de rendimiento debido a la mayor comunicación y duplicación de los datos necesarios para que el entorno de scripting interactúe con el componente. Al usar servicios sin componentes, estos costos se minimizan.

Los temas descritos en la tabla siguiente proporcionan información general y de tareas sobre el uso de servicios COM+ sin componentes. Esta característica está pensada para desarrolladores avanzados Visual C++ que están interesados en el rendimiento.



| Tema                                                                                                 | Descripción                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Conceptos de servicios COM+ sin componentes](com--services-without-components-concepts.md)<br/> | Proporciona información general sobre el uso de servicios COM+ sin componentes.<br/>                     |
| [Tareas servicios COM+ sin componentes](com--services-without-components-tasks.md)<br/>       | Proporciona instrucciones para usar COM+ para crear y usar servicios sin componentes.<br/> |



 

 

 




