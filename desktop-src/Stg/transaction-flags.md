---
title: Marcas de transacción
description: Un objeto se puede abrir en modo directo o de transacción.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268944"
---
# <a name="transaction-flags"></a>Marcas de transacción

Un objeto se puede abrir en modo directo o de transacción. Cuando un objeto se abre en modo directo, los cambios se realizan de forma inmediata y permanente. Cuando se abre un objeto en modo de transacción, los cambios se almacenan en búfer para que se puedan confirmar o revertir explícitamente una vez completada la edición. Los cambios confirmados se guardan en el objeto mientras se descartan los cambios revertidos. El modo directo es el modo de acceso predeterminado.

No es necesario el modo de transacción en un objeto de almacenamiento primario para poder usarlo en un elemento anidado. Sin embargo, una transacción para un elemento anidado está anidada dentro de la transacción para su objeto de almacenamiento primario. Por lo tanto, los cambios realizados en un objeto secundario no se pueden confirmar hasta que se confirmen los que se realizan en el elemento primario y ambos permanecen sin confirmar hasta que el objeto de almacenamiento raíz (el primario de nivel superior) se escribe realmente en el disco. En otras palabras, los cambios se mueven hacia fuera: los objetos internos publican los cambios en las transacciones de sus contenedores inmediatos.

 

 




