---
description: La clase CMSPThread implementa el subproceso de trabajo de MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992efdc7f46772ee7766ba38ebab4cf3a9adc502e7c4001eb91779d03c677d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946681"
---
# <a name="cmspthread"></a>CMSPThread

La **clase CMSPThread** implementa el subproceso de trabajo del MSP. Las clases base usan este subproceso de trabajo para una serie de propósitos. Se proporciona un mecanismo de elemento de trabajo genérico y ligero para permitir que el MSP derivado use este subproceso para sus propios elementos de trabajo sincrónicos o asincrónicos, sean cuales sean. El subproceso también proporciona mensajes y admite el control de las API (aunque las API no se usan en las clases base).

Cuando hay varias direcciones de tipo presentes (es decir, cuando se crea una instancia de la misma implementación de MSP desde el mismo archivo DLL varias veces), la clase de subproceso garantiza la escalabilidad mediante el uso automático de un único subproceso para todas las direcciones. La interfaz a la clase de subproceso es tal que la implementación de MSP puede pensar en la clase de subproceso como un subproceso privado y no necesita importar las otras direcciones que pueden compartirla.

Definido en MSPthrd.h.

 

 



