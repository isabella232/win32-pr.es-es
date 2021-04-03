---
description: El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en sistemas basados en Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: El Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809853"
---
# <a name="the-volume-shadow-copy-service"></a>El Servicio de instantáneas de volumen

El Servicio de instantáneas de volumen (VSS) proporciona la infraestructura del sistema para ejecutar aplicaciones VSS en sistemas basados en Windows.

Aunque es muy transparente para el usuario y el desarrollador, VSS hace lo siguiente:

-   Coordina las actividades de proveedores, escritores y solicitantes en la creación y el uso de instantáneas
-   Facilita el proveedor del sistema predeterminado
-   Implementa la funcionalidad de controlador de bajo nivel necesaria para que cualquier proveedor funcione

El servicio VSS se inicia a petición, de modo que, para que las operaciones de VSS se realicen correctamente, este servicio debe estar habilitado.

 

 



