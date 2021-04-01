---
description: Descripción de las formas de mejorar el rendimiento al usar las interfaces de programación de aplicaciones (API) de StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Consideraciones de rendimiento para la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818099"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Consideraciones de rendimiento para la API de StylusInput

En la lista siguiente se describen algunas formas de mejorar el rendimiento de las aplicaciones que usan las API de StylusInput.

-   Use la propiedad [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms824769(v=msdn.10)) para suscribirse solo a los datos relevantes para el complemento. Esto reduce el número total de llamadas al método que realiza el objeto [**RealTimeStylus**](realtimestylus-class.md) y también reduce la complejidad del complemento. El objeto **RealTimeStylus** solo comprueba la propiedad de interés cuando se adjunta el complemento.
-   Minimizar la complejidad de los complementos sincrónicos. Los complementos sincrónicos generalmente son llamados por el subproceso del objeto [**RealTimeStylus**](realtimestylus-class.md) y pueden contribuir a retrasos en la recopilación de entradas manuscritas.
-   Considere la posibilidad de convertir el complemento en asincrónico. Si el complemento es complejo y necesita agregar datos personalizados a la cola del objeto [**RealTimeStylus**](realtimestylus-class.md) , considere la posibilidad de usar un modelo **RealTimeStylus** en cascada y agregar el complemento a la colección de complementos sincrónicos del objeto **RealTimeStylus** secundario. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

 

 
