---
description: Algunos objetos solo admiten un identificador a la vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Control de limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243956"
---
# <a name="handle-limitations"></a>Control de limitaciones

Algunos objetos solo admiten un identificador a la vez. El sistema proporciona el identificador cuando una aplicación crea el objeto e invalida el identificador cuando la aplicación destruye el objeto. Otros objetos admiten varios identificadores para un solo objeto. El sistema operativo quita automáticamente el objeto de la memoria después de cerrar el último identificador del objeto.

El número total de identificadores abiertos en el sistema solo está limitado por la cantidad de memoria disponible. Algunos tipos de objeto admiten un número limitado de identificadores por sesión o por proceso.

 

 



