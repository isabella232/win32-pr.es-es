---
title: Tipos de notificaciones
description: Tipos de notificaciones
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160521"
---
# <a name="types-of-notifications"></a>Tipos de notificaciones

Las notificaciones se agrupan en tres grupos: documento compuesto, datos y vista. Un objeto envía notificaciones de documentos compuestos en respuesta a que se cambie el nombre, se guarde, se cierre o, en el caso de un vínculo, se cambie el nombre del origen del vínculo. Como se esperaría, los objetos envían notificaciones de datos en respuesta a los cambios en sus datos y envían notificaciones de vista en respuesta a los cambios en su presentación. Las aplicaciones de contenedor deben registrarse por separado para cada uno de estos tipos de notificación, pero todas pueden controlarse mediante un único receptor de aviso.

Todos los contenedores, el controlador de objetos y el registro de objetos vinculados para las notificaciones de documentos compuestos. El contenedor típico también se registra para ver las notificaciones. Normalmente, las notificaciones de datos se envían al objeto vinculado y al controlador de objetos. Un contenedor de propósito especial, como uno que representa los propios datos, podría beneficiarse de recibir notificaciones de datos en lugar de ver las notificaciones. Por ejemplo, un contenedor de gráficos incrustados con un vínculo a una tabla puede registrarse para recibir notificaciones de datos. Dado que un cambio en la tabla afecta al gráfico, la recepción de una notificación de datos dirigiría al contenedor a obtener los nuevos datos tabulares.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificaciones](notifications.md)
</dt> </dl>

 

 




