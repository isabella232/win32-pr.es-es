---
title: Tipos de notificaciones
description: Tipos de notificaciones
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418975"
---
# <a name="types-of-notifications"></a>Tipos de notificaciones

Las notificaciones se dividen en tres grupos: documento compuesto, datos y vista. Un objeto envía notificaciones de documentos compuestos en respuesta a que se les cambia el nombre, se guardan, se cierran o, en el caso de un vínculo, se cambia el nombre del origen del vínculo. Como cabría esperar, los objetos envían notificaciones de datos en respuesta a los cambios en sus datos y envían notificaciones de vista en respuesta a los cambios en su presentación. Las aplicaciones de contenedor se deben registrar por separado para cada uno de estos tipos de notificación, pero todo se puede controlar mediante un único receptor de consulta.

Todos los contenedores, el controlador de objetos y el objeto vinculado se registran para las notificaciones de documentos compuestos. El contenedor típico también se registra para las notificaciones de vista. Las notificaciones de datos normalmente se envían al objeto vinculado y al controlador de objetos. Un contenedor de propósito especial, como uno que representa los datos en sí, puede beneficiarse de la recepción de notificaciones de datos en lugar de ver las notificaciones. Por ejemplo, un contenedor de gráficos incrustado con un vínculo a una tabla puede registrarse para recibir notificaciones de datos. Dado que un cambio en la tabla afecta al gráfico, la recepción de una notificación de datos dirigiría el contenedor para obtener los nuevos datos tabulares.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificaciones](notifications.md)
</dt> </dl>

 

 




