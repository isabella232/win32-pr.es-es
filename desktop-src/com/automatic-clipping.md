---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357421"
---
# <a name="automatic-clipping"></a>Recorte automático

Se recomienda encarecidamente que un contenedor de controles ActiveX admita el recorte automático de sus controles. Esto dará lugar a una operación más eficaz para la mayoría de los controles. Si se admite el recorte automático, se debe admitir la propiedad de ambiente AutoClip y tener un valor de **true**.

El recorte automático es la capacidad de un contenedor para asegurarse de que la salida dibujada de un control solo se dirige a la región de recorte actual del contenedor. En un contenedor que admite el recorte automático, un control puede pintar sin tener en cuenta su región de recorte, ya que el contenedor recortará automáticamente cualquier dibujo que se produzca fuera del área del control. Si un contenedor no admite el recorte automático, los controles generados por el CDK crearán una ventana primaria adicional si se pasa una región de recorte que no sea NULL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




