---
title: Rutas estáticas y autoestáticas
description: Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994509"
---
# <a name="static-and-autostatic-routes"></a>Rutas estáticas y autoestáticas

Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento. Sin embargo, el administrador también puede *inicializar* la tabla de enrutamiento proporcionando rutas manualmente. Estas rutas se conocen como *estáticas*. Una ruta estática está asociada a una interfaz que representa la red remota. A diferencia de las rutas dinámicas, las rutas estáticas se conservan incluso si el enrutador se reinicia o la interfaz está deshabilitada.

Una ruta *autoestática* se obtiene a través de un protocolo de enrutamiento, pero una vez obtenida se comporta como una ruta estática. El proceso para obtener rutas autoestáticas es el siguiente: el administrador de enrutadores IP o IPX emite una solicitud para que un protocolo de enrutamiento actualice la información de enrutamiento de una interfaz específica. Los resultados de la actualización se convierten después en rutas estáticas. Tenga en cuenta que solo determinados protocolos de enrutamiento admiten solicitudes de actualizaciones de rutas autoestáticas.

 

 




