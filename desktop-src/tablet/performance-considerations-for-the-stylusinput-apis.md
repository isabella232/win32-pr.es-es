---
description: Descripción de las formas de mejorar el rendimiento al usar las interfaces de programación de aplicaciones (API) StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Consideraciones de rendimiento para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef40ab389687cd42ef516a61f61ab86a7eb79d4efac9ae6e9dd698e93e54bff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856497"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Consideraciones de rendimiento para StylusInput API

En la lista siguiente se describen algunas maneras de mejorar el rendimiento de las aplicaciones que usan las API StylusInput.

-   Use la propiedad [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) para suscribirse solo a los datos pertinentes para el complemento. Esto reduce el número total de llamadas de método que realiza el objeto [**RealTimeStylus**](realtimestylus-class.md) y también reduce la complejidad del complemento. El **objeto RealTimeStylus** solo comprueba la propiedad DataInterest cuando se adjunta el complemento.
-   Minimice la complejidad de los complementos sincrónicos. Complementos sincrónicos que normalmente llama el subproceso del objeto [**RealTimeStylus**](realtimestylus-class.md) y pueden contribuir a retrasos en la recopilación de entrada de lápiz.
-   Considere la posibilidad de convertir el complemento en asincrónico. Si el complemento es complejo y necesita agregar datos personalizados a la cola del objeto [**RealTimeStylus,**](realtimestylus-class.md) considere la posibilidad de usar un modelo **RealTimeStylus** en cascada y agregar el complemento a la colección sincrónica del objeto **RealTimeStylus** secundario. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

 

 
