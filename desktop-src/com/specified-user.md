---
title: Usuario especificado
description: Usuario especificado
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704610"
---
# <a name="specified-user"></a>Usuario especificado

Especificar un usuario determinado (y la contraseña del usuario) es la identidad preferida para los servidores COM. La razón por la que se prefiere esta identidad es que no se tiene que registrar ninguna en el equipo en el que se ejecuta el servidor y que cada cliente se comunica con la misma instancia del servidor si el servidor registra su generador de clases como multiuso. Si el servidor tiene una GUI, no debe elegir esta identidad; Si lo hace, el usuario no podrá ver la interfaz de usuario.

Este tipo de servidor tiene un token principal y puede tener acceso a recursos remotos en los que un servidor que tenga la identidad de inicio-usuario podría no ser capaz de hacerlo. Para obtener más información sobre la suplantación y los tokens de acceso, vea [niveles de suplantación](impersonation-levels.md) y [ocultación](cloaking.md).

Ejecutar como cuenta de usuario fijo es más seguro que la identidad de usuario interactiva, ya que solo alguien que tenga la contraseña de usuario específica puede asignar esta identidad a la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identidad de la aplicación](application-identity.md)
</dt> <dt>

[Usuario interactivo](interactive-user.md)
</dt> <dt>

[Iniciando usuario](launching-user.md)
</dt> <dt>

[Identidad de servicio](service-identity.md)
</dt> </dl>

 

 




