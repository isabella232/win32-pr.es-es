---
description: El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en Windows basados en aplicaciones.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: El Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866245"
---
# <a name="the-volume-shadow-copy-service"></a>El Servicio de instantáneas de volumen

El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en Windows basados en aplicaciones.

Aunque es en gran medida transparente para el usuario y el desarrollador, VSS hace lo siguiente:

-   Coordina las actividades de proveedores, escritores y solicitantes en la creación y el uso de instantáneas
-   Se utiliza el proveedor del sistema predeterminado
-   Implementa la funcionalidad de controlador de bajo nivel necesaria para que cualquier proveedor funcione

El servicio VSS se inicia a petición, de modo que, para que las operaciones de VSS se realicen correctamente, este servicio debe estar habilitado.

 

 



