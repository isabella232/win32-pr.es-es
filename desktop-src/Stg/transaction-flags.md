---
title: Marcas de transacción
description: Un objeto se puede abrir en modo directo o en modo de transacción.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270548"
---
# <a name="transaction-flags"></a>Marcas de transacción

Un objeto se puede abrir en modo directo o en modo de transacción. Cuando se abre un objeto en modo directo, los cambios se realizan de forma inmediata y permanente. Cuando se abre un objeto en modo de transacción, los cambios se almacena en búfer para que se puedan confirmados o revertido explícitamente una vez completada la edición. Los cambios confirmados se guardan en el objeto mientras se descartan los cambios revertido. El modo directo es el modo de acceso predeterminado.

El modo de transacción no es necesario en un objeto de almacenamiento primario para usarlo en un elemento anidado. Sin embargo, una transacción para un elemento anidado está anidada dentro de la transacción para su objeto de almacenamiento primario. Por lo tanto, los cambios realizados en un objeto secundario no se pueden confirmar hasta que se confirman los realizados en el elemento primario y ambos permanecen sin confirmar hasta que el objeto de almacenamiento raíz (el elemento primario de nivel superior) se escribe realmente en el disco. En otras palabras, los cambios se mueven hacia el exterior: los objetos internos publican cambios en las transacciones de sus contenedores inmediatos.

 

 




