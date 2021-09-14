---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360873"
---
# <a name="automatic-clipping"></a>Recorte automático

Se recomienda encarecidamente que un contenedor ActiveX control admita el recorte automático de sus controles. Esto dará como resultado un funcionamiento más eficaz para la mayoría de los controles. Si se admite el recorte automático, la propiedad ambiente AutoClip debe ser compatible y tener un valor de **TRUE.**

El recorte automático es la capacidad de un contenedor para asegurarse de que la salida dibujada de un control solo va a la región de recorte actual del contenedor. En un contenedor que admite el recorte automático, un control puede pintar sin tener en cuenta su región de recorte, ya que el contenedor recortará automáticamente cualquier dibujo que se produzca fuera del área del control. Si un contenedor no admite el recorte automático, los controles generados por CDK crearán una ventana primaria adicional si se pasa una región de recorte que no es NULL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




