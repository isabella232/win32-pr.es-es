---
title: Servicios de autorización
description: Un servicio de autorización es el método que el SSP usa para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476618"
---
# <a name="authorization-services"></a>Servicios de autorización

Un servicio de autorización es el método que el SSP usa para autorizar el acceso a un procedimiento remoto. Los SSP pueden proporcionar más de un servicio de autorización. Sin embargo, normalmente seleccionan uno como valor predeterminado.

La aplicación puede usar el método de autorización predeterminado para el SSP actual o puede especificar uno. En la actualidad, Rpc de Microsoft admite dos métodos de autorización. Una es para que el servidor proporcione autorización basada en el nombre del programa cliente. La otra es que el servidor compare las credenciales de autenticación del cliente con la lista de control de acceso (ACL) del servidor.

Para obtener una lista de servicios de autorización, vea [Constantes de authorization-service](authorization-service-constants.md).

> [!Note]  
> Se recomienda que los desarrolladores usen RPC \_ C \_ AUTHZ \_ NONE.

 

 

 




