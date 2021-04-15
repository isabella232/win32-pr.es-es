---
description: Marcas de coherencia y de realización
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Marcas de coherencia y de realización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539430"
---
# <a name="consistent-and-done-flags"></a>Marcas de coherencia y de realización

COM+ siempre crea un objeto de contexto antes de activar un objeto transaccional. El objeto de contexto contiene información relacionada con el objeto, como su creador y su identificador de transacción. Cada objeto de contexto también contiene una marca *coherente* y una *marca Done*. Juntas, estas marcas determinan el estado del objeto transaccional.

La marca coherente indica que el objeto transaccional es coherente o incoherente. Los detalles específicos de lo que hace que el estado de un objeto sea coherente es el programador. Cuando una llamada al método establece esta marca en true, el objeto es coherente. False indica que el objeto es incoherente. COM+ establece la marca en true cuando crea una instancia de objeto. Un objeto coherente está listo para continuar con la transacción. Mientras un objeto permanece activo, las llamadas posteriores al método pueden cambiar repetidamente la marca coherente de true a false y viceversa.

La marca Done determina la duración de una transacción. Cuando una llamada de método devuelve, COM+ inspecciona la marca done. Si el método establece esta marca en true, COM+ desactiva el objeto y anota la marca coherente. Cuando la marca Done es false, COM+ no desactiva el objeto ni anota la marca coherente. COM+ establece la marca done en false cuando crea una instancia de objeto.

La marca coherente convierte un voto para confirmar o anular la transacción en la que se ejecuta, y la marca Done finaliza el voto. COM+ inspecciona la marca coherente cuando la marca Done está establecida en true en una llamada al método que devuelve o cuando el objeto se desactiva. Aunque la marca coherente de un objeto puede cambiar repetidamente dentro de cada llamada al método, solo el último cambio cuenta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Establecimiento de las marcas coherente y realizada](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



