---
description: La clase CMSPThread implementa el subproceso de trabajo de los MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678362"
---
# <a name="cmspthread"></a>CMSPThread

La clase **CMSPThread** implementa el subproceso de trabajo de MSP. Las clases base utilizan este subproceso de trabajo para varios propósitos. Se proporciona un mecanismo de elementos de trabajo genéricos y ligeros para permitir que el MSP derivado use este subproceso para sus propios elementos de trabajo sincrónicos o asincrónicos, lo que sea posible. El subproceso también bombea mensajes y admite el control de APC (aunque APC no se usan en las clases base).

Cuando hay varias direcciones similares (es decir, cuando se crea una instancia de la misma implementación MSP del mismo archivo DLL varias veces), la clase de subproceso garantiza la escalabilidad mediante el uso automático de un único subproceso para todas las direcciones. La interfaz a la clase de subproceso es de tal modo que la implementación de MSP puede pensar en la clase de subproceso como un subproceso privado y no necesita preocuparse por las demás direcciones que pueden compartirla.

Definido en MSPthrd. h.

 

 



