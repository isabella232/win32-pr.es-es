---
description: Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de unión. Los cambios que realice en la instancia de clase de vista se propagarán de nuevo a las instancias de clase de origen que forman la clase de vista de unión.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Actualizar una vista de unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7061181971a6f97a0bbde0992b64a8bdb3be8c7441fb4e90cb8fdcd0d675a221
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030335"
---
# <a name="updating-a-union-view"></a>Actualizar una vista de unión

Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de unión. Los cambios que realice en la instancia de clase de vista se propagarán de nuevo a las instancias de clase de origen que forman la clase de vista de unión.

Las restricciones siguientes se aplican a los cambios para ver instancias de clase:

-   No se pueden crear nuevas instancias de clases de vista.
-   Solo las clases de unión admiten actualizaciones; Las vistas de combinación y asociación crean instancias de vista de solo lectura.
-   El éxito de una actualización depende de si una instancia de origen se puede actualizar. Si una propiedad de instancia de vista se asigna a una propiedad de solo lectura de una instancia de origen, se producirá un error al intentar modificar la propiedad de vista.

 

 



