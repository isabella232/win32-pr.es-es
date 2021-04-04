---
title: Métodos de seguridad
description: Microsoft RPC admite dos métodos diferentes para agregar seguridad a la aplicación distribuida.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076175"
---
# <a name="security-methods"></a>Métodos de seguridad

Microsoft RPC admite dos métodos diferentes para agregar seguridad a la aplicación distribuida. El primer método consiste en usar la interfaz del proveedor de compatibilidad para seguridad (SSPI), a la que se puede tener acceso mediante las funciones RPC. En general, es mejor utilizar este método. SSPI proporciona las características de autenticación más flexibles y independientes de la red.

El segundo método consiste en utilizar las características de seguridad integradas en los protocolos de transporte del sistema. El método de seguridad de nivel de transporte no es el método preferido. Se recomienda usar SSPI porque funciona en todos los transportes, entre plataformas, y proporciona altos niveles de seguridad, incluida la privacidad.

En esta sección se proporciona información general sobre la seguridad de nivel de transporte y SSPI en los temas siguientes:

-   [Interfaz del proveedor de compatibilidad con seguridad (SSPI)](security-support-provider-interface-sspi-.md)
-   [Seguridad de transporte](transport-security.md)

 

 




