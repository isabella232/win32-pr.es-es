---
description: Marcas coherentes y realizadas
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Marcas coherentes y realizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b0c614c745f46d8bbcc816b65f501e02de1e0455f0b64216662ec52308213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954365"
---
# <a name="consistent-and-done-flags"></a>Marcas coherentes y realizadas

COM+ siempre crea un objeto de contexto antes de activar un objeto transaccional. El objeto de contexto contiene información relacionada con objetos, como su creador y su identificador de transacción. Cada objeto de contexto también contiene una *marca coherente y* una marca *done*. Juntas, estas marcas determinan el estado del objeto transaccional.

La marca coherente indica que el objeto transaccional es coherente o incoherente. Los detalles específicos de lo que hace que el estado de un objeto sea coherente son del programador. Cuando una llamada de método establece esta marca en True, el objeto es coherente. False indica que el objeto es incoherente. COM+ establece la marca en True cuando crea una instancia de objeto. Un objeto coherente está listo para continuar con la transacción. Mientras un objeto permanece activo, las llamadas a métodos posteriores pueden cambiar repetidamente la marca coherente de True a False y viceversa.

La marca done determina la duración de una transacción. Cuando se devuelve una llamada de método, COM+ inspecciona la marca done. Si el método establece esta marca en True, COM+ desactiva el objeto y toma nota de la marca coherente. Cuando la marca done es False, COM+ no desactiva el objeto ni anota la marca coherente. COM+ establece la marca done en False cuando crea una instancia de objeto.

La marca coherente convierte un voto para confirmar o anular la transacción en la que se ejecuta, y la marca done finalizará el voto. COM+ inspecciona la marca coherente cuando la marca done se establece en True en una devolución de llamada de método o cuando el objeto se desactiva. Aunque la marca coherente de un objeto puede cambiar repetidamente dentro de cada llamada de método, solo cuenta el último cambio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Establecimiento de las marcas Coherente y Listo](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



