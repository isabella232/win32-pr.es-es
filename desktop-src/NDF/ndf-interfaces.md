---
title: Interfaces NDF
description: Las siguientes interfaces se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074995"
---
# <a name="ndf-interfaces"></a>Interfaces NDF

Las siguientes interfaces se pueden usar para ampliar la funcionalidad de las clases auxiliares de Microsoft que se identifican como extensibles. Aunque esta funcionalidad no es necesaria para la mayoría de las aplicaciones, puede proporcionar diagnósticos y resoluciones más específicos en algunos casos.

> [!Note]  
> Estas interfaces y sus métodos asociados son para desarrolladores que implementan sus propias clases auxiliares de terceros que amplían la funcionalidad NDF.

 



| Nombre de la interfaz                                                 | Descripción                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Lo llama el NDF para la mayoría de las actividades que se producen durante un diagnóstico.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Lo llama el NDF para capturar y proporcionar información asociada con los diagnósticos y la resolución de problemas relacionados con la red. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Lo llama el NDF para validar que tiene información necesaria                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Reservado para uso del sistema.                                                                                                 |



 

 

 




