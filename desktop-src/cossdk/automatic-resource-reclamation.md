---
description: Recuperación automática de recursos
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recuperación automática de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360057"
---
# <a name="automatic-resource-reclamation"></a>Recuperación automática de recursos

COM+ notifica al administrador dispensador cada vez que finaliza la duración de un objeto. A continuación, el administrador de dispensadores notifica a cada titular de un dispensador de recursos registrados para ver si tiene algún recurso que todavía tenga este objeto. Si es así, se liberan esos recursos, lo que evita la posibilidad de que se produzcan pérdidas de recursos por parte de los componentes que obtienen recursos a través de un dispensador de recursos.

La característica de recuperación automática es una opción que está desactivada de forma predeterminada. Un dispensador de recursos puede optar por habilitar esta opción y, al hacerlo, garantiza que los métodos de objeto nunca devuelven una referencia a los recursos dispensados en un objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



