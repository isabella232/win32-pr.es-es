---
description: Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de Unión. Los cambios que realice en la instancia de la clase de vista se propagarán de nuevo a las instancias de la clase de origen que forman la clase de vista Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Actualizar una vista de Unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155805"
---
# <a name="updating-a-union-view"></a>Actualizar una vista de Unión

Puede actualizar los valores de las propiedades sin clave de las instancias de clase de vista de Unión. Los cambios que realice en la instancia de la clase de vista se propagarán de nuevo a las instancias de la clase de origen que forman la clase de vista Union.

Las siguientes restricciones se aplican a los cambios en las instancias de la clase de vista:

-   No se pueden crear nuevas instancias de clases de vista.
-   Solo las clases Union admiten actualizaciones; las vistas de combinación y de asociación crean instancias de vista de solo lectura.
-   El éxito de una actualización depende de si una instancia de origen es actualizable. Si una propiedad de instancia de vista se asigna a una propiedad de solo lectura de una instancia de origen, se producirá un error al intentar modificar la propiedad de vista.

 

 



