---
title: NDF Interfaces
description: Las interfaces siguientes se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16ff5dde9246798392903f47370e663e26dd6be7f21252f8791bfee267018b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801955"
---
# <a name="ndf-interfaces"></a>NDF Interfaces

Las interfaces siguientes se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles. Aunque esta funcionalidad no es necesaria para la mayoría de las aplicaciones, puede proporcionar diagnósticos y soluciones más específicos en algunos casos.

> [!Note]  
> Estas interfaces y sus métodos asociados son para desarrolladores que implementan sus propias clases auxiliares de terceros que amplían la funcionalidad de NDF.

 



| Nombre de la interfaz                                                 | Descripción                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Lo llama el NDF para la mayoría de las actividades que se producen durante un diagnóstico.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Lo llama NDF para capturar y proporcionar información asociada a diagnósticos y resolución de problemas relacionados con la red. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Llamado por el NDF para validar que tiene la información necesaria                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Reservado para uso del sistema.                                                                                                 |



 

 

 




