---
title: Iniciar usuario
description: Iniciar usuario
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359842"
---
# <a name="launching-user"></a>Iniciar usuario

Esta es la configuración predeterminada para la identidad de la aplicación. Cuando se elige el usuario de inicio para la identidad de la aplicación, cada cuenta de cliente obtiene una nueva instancia del servidor y cada servidor obtiene su propia estación [de ventana](/windows/desktop/winstation/window-stations). Debido a las instancias de servidor independientes, iniciar el usuario es la configuración de identidad de protección de seguridad de nivel superior. Sin embargo, hay límites finitos en el consumo de recursos. Además, el cliente no verá ninguna GUI que muestre el servidor.

Si la aplicación tiene la identidad del usuario de inicio, se ejecuta con un token de suplantación. Para obtener más información sobre la suplantación y los tokens de acceso, vea Niveles de [suplantación](impersonation-levels.md) y [Desenlazamiento.](cloaking.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identidad de aplicación](application-identity.md)
</dt> <dt>

[Usuario interactivo](interactive-user.md)
</dt> <dt>

[Identidad de servicio](service-identity.md)
</dt> <dt>

[Usuario especificado](specified-user.md)
</dt> </dl>

 

 