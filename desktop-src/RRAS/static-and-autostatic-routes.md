---
title: Rutas estáticas y autostáticas
description: Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171306"
---
# <a name="static-and-autostatic-routes"></a>Rutas estáticas y autostáticas

Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento. Sin embargo, el administrador también *puede establecer la tabla* de enrutamiento proporcionando rutas manualmente. Estas rutas se conocen como *estáticas.* Una ruta estática está asociada a una interfaz que representa la red remota. A diferencia de las rutas dinámicas, las rutas estáticas se conservan incluso si el enrutador se reinicia o la interfaz está deshabilitada.

Una *ruta estática automática* se obtiene a través de un protocolo de enrutamiento, pero una vez obtenido se comporta como una ruta estática. El proceso para obtener rutas estáticas automáticas es el siguiente: el administrador de enrutadores IP o IPX emite una solicitud para que un protocolo de enrutamiento actualice la información de enrutamiento de una interfaz específica. A continuación, los resultados de la actualización se convierten en rutas estáticas. Tenga en cuenta que solo determinados protocolos de enrutamiento admiten solicitudes de actualizaciones de rutas estáticas automáticas.

 

 




