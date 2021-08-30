---
title: Métodos de seguridad
description: Rpc de Microsoft admite dos métodos diferentes para agregar seguridad a la aplicación distribuida.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac09f29c4912228207e5c09d4551f408a76788d3d3ecf999aae2fcc1c63ded6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018043"
---
# <a name="security-methods"></a>Métodos de seguridad

Rpc de Microsoft admite dos métodos diferentes para agregar seguridad a la aplicación distribuida. El primer método consiste en usar la interfaz del proveedor de compatibilidad de seguridad (SSPI), a la que se puede acceder mediante las funciones RPC. En general, es mejor usar este método. SSPI proporciona las características de autenticación más flexibles e independientes de la red.

El segundo método consiste en usar las características de seguridad integradas en los protocolos de transporte del sistema. El método de seguridad de nivel de transporte no es el método preferido. Se recomienda usar SSPI porque funciona en todos los transportes, entre plataformas y proporciona altos niveles de seguridad, incluida la privacidad.

En esta sección se proporcionan información general sobre SSPI y la seguridad de nivel de transporte en los temas siguientes:

-   [Interfaz del proveedor de compatibilidad con seguridad (SSPI)](security-support-provider-interface-sspi-.md)
-   [Seguridad de transporte](transport-security.md)

 

 




