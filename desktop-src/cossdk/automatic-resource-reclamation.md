---
description: Recuperación automática de recursos
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recuperación automática de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465577"
---
# <a name="automatic-resource-reclamation"></a>Recuperación automática de recursos

COM+ notifica al administrador del distribuidor cada vez que finaliza la duración de un objeto. A continuación, el administrador del dispensador notifica al titular de cada distribuidor de recursos registrado que vea si todavía tiene algún recurso en poder de este objeto. Si es así, esos recursos se liberan, lo que impide la posibilidad de pérdidas de recursos por parte de los componentes que obtienen recursos a través de un distribuidor de recursos.

La característica de reclamación automática es una opción que está desactivada de forma predeterminada. Un dispensador de recursos puede optar por habilitar esta opción y, al hacerlo, garantiza que los métodos de objeto nunca devuelven una referencia a cualquier recurso que se distribuyó a un objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



