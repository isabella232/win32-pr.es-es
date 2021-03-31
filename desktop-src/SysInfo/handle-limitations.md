---
description: Algunos objetos solo admiten un identificador a la vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Solucionar limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278789"
---
# <a name="handle-limitations"></a>Solucionar limitaciones

Algunos objetos solo admiten un identificador a la vez. El sistema proporciona el identificador cuando una aplicación crea el objeto e invalida el identificador cuando la aplicación destruye el objeto. Otros objetos admiten varios identificadores para un único objeto. El sistema operativo quita automáticamente el objeto de la memoria después de cerrarse el último identificador del objeto.

El número total de identificadores abiertos en el sistema solo está limitado por la cantidad de memoria disponible. Algunos tipos de objetos admiten un número limitado de identificadores por sesión o por proceso.

 

 



