---
title: Servicios de autorización
description: Un servicio de autorización es el método que usa el SSP para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076032"
---
# <a name="authorization-services"></a>Servicios de autorización

Un servicio de autorización es el método que usa el SSP para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.

La aplicación puede utilizar el método de autorización predeterminado para el SSP actual o puede especificar uno. En la actualidad, Microsoft RPC admite dos métodos de autorización. Uno es para que el servidor proporcione autorización basada en el nombre del programa cliente. El otro es para que el servidor Compare las credenciales de autenticación del cliente con la lista de control de acceso (ACL) del servidor.

Para obtener una lista de servicios de autorización, consulte [constantes de servicio de autorización](authorization-service-constants.md).

> [!Note]  
> Se recomienda que los desarrolladores usen RPC \_ C \_ AUTHZ \_ None.

 

 

 




