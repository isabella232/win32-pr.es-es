---
title: Interfaces privadas de Container-Specific
description: Interfaces privadas de Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357693"
---
# <a name="container-specific-private-interfaces"></a>Interfaces privadas de Container-Specific

Algunos contenedores proporcionan interfaces privadas específicas del contenedor para una funcionalidad adicional o un rendimiento mejorado. Los controles que dependen de esas interfaces específicas del contenedor deberían, si es posible, trabajar sin esas interfaces específicas del contenedor para que el control funcione en contenedores diferentes. Por ejemplo, Visual Basic implementa interfaces privadas que proporcionan la funcionalidad de formato de cadena para los controles. Si un control usa estas interfaces de formato privado, debería poder ejecutarse con compatibilidad de formato predeterminada si estas interfaces no están disponibles. Si el control puede funcionar sin las interfaces privadas, debe llevar a cabo la acción adecuada (por ejemplo, advertir al usuario de la funcionalidad reducida) pero seguir trabajando. Si no es una opción, se debe registrar una categoría de componente como sea necesario para que solo los contenedores que admiten esta funcionalidad puedan hospedar estos controles.

 

 




