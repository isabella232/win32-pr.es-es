---
title: Servicios de autorización
description: Un servicio de autorización es el método que el SSP usa para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef09377ae70d36b6d4eb7aa87794669bf247842d109cec87852db9970ea8c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023425"
---
# <a name="authorization-services"></a>Servicios de autorización

Un servicio de autorización es el método que el SSP usa para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.

La aplicación puede usar el método de autorización predeterminado para el SSP actual o puede especificar uno. En la actualidad, Rpc de Microsoft admite dos métodos de autorización. Una es para que el servidor proporcione autorización basada en el nombre del programa cliente. La otra es que el servidor compare las credenciales de autenticación del cliente con la lista de control de acceso (ACL) del servidor.

Para obtener una lista de servicios de autorización, vea [Constantes de authorization-service](authorization-service-constants.md).

> [!Note]  
> Se recomienda que los desarrolladores usen RPC \_ C \_ AUTHZ \_ NONE.

 

 

 




