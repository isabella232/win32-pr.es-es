---
title: Container-Specific privadas
description: Container-Specific privadas
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a426ae67d3722406ca6c1428d46d0bc3b4a937a1bcdd105de6f376bbe53a5ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550639"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific privadas

Algunos contenedores proporcionan interfaces privadas específicas del contenedor para una funcionalidad adicional o un rendimiento mejorado. Los controles que se basan en esas interfaces específicas del contenedor deben funcionar, si es posible, sin esas interfaces específicas del contenedor presentes para que el control funcione en contenedores diferentes. Por ejemplo, Visual Basic implementa interfaces privadas que proporcionan funcionalidad de formato de cadena a los controles. Si un control usa estas interfaces de formato privado, debería poder ejecutarse con compatibilidad de formato predeterminada si estas interfaces no están disponibles. Si el control puede funcionar sin las interfaces privadas, debe tomar las medidas adecuadas (por ejemplo, advertir al usuario de una funcionalidad reducida) pero seguir trabajando. Si esta no es una opción, se debe registrar una categoría de componente como necesaria para que solo los contenedores que admitan esta funcionalidad puedan hospedar estos controles.

 

 




