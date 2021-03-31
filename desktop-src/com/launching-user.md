---
title: Iniciando usuario
description: Iniciando usuario
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904841"
---
# <a name="launching-user"></a>Iniciando usuario

Esta es la configuración predeterminada para la identidad de la aplicación. Cuando se elige el usuario iniciador para la identidad de la aplicación, cada cuenta de cliente obtiene una nueva instancia del servidor y cada servidor obtiene su propia [estación de ventana](/windows/desktop/winstation/window-stations). Debido a las instancias de servidor independientes, el usuario que inicia es el valor de identidad de protección de seguridad de nivel superior. Sin embargo, hay límites finitos en el consumo de recursos. Además, el cliente no verá las GUI que muestre el servidor.

Si la aplicación tiene la identidad del usuario que inicia, se ejecuta con un token de suplantación. Para obtener más información sobre la suplantación y los tokens de acceso, vea [niveles de suplantación](impersonation-levels.md) y [ocultación](cloaking.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identidad de la aplicación](application-identity.md)
</dt> <dt>

[Usuario interactivo](interactive-user.md)
</dt> <dt>

[Identidad de servicio](service-identity.md)
</dt> <dt>

[Usuario especificado](specified-user.md)
</dt> </dl>

 

 