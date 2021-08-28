---
title: Rutas estáticas y autostáticas
description: Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127835"
---
# <a name="static-and-autostatic-routes"></a>Rutas estáticas y autostáticas

Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento. Sin embargo, el administrador también *puede establecer la tabla* de enrutamiento proporcionando rutas manualmente. Estas rutas se conocen como *estáticas.* Una ruta estática está asociada a una interfaz que representa la red remota. A diferencia de las rutas dinámicas, las rutas estáticas se conservan incluso si el enrutador se reinicia o la interfaz está deshabilitada.

Una *ruta estática se* obtiene a través de un protocolo de enrutamiento, pero una vez obtenida se comporta como una ruta estática. El proceso para obtener rutas estáticas automáticas es el siguiente: el administrador de enrutadores IP o IPX emite una solicitud para que un protocolo de enrutamiento actualice la información de enrutamiento de una interfaz específica. A continuación, los resultados de la actualización se convierten en rutas estáticas. Tenga en cuenta que solo determinados protocolos de enrutamiento admiten solicitudes de actualizaciones de rutas estáticas automáticas.

 

 




