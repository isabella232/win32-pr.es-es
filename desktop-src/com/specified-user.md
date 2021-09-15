---
title: Usuario especificado
description: Usuario especificado
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360160"
---
# <a name="specified-user"></a>Usuario especificado

Especificar un usuario determinado (y la contraseña del usuario) es la identidad preferida para los servidores COM. La razón por la que se prefiere esta identidad es que nadie tiene que iniciar sesión en el equipo en el que se ejecuta el servidor para que se ejecute, y cada cliente se pone en conversación con la misma instancia del servidor si el servidor registra su generador de clases como multiuso. Si el servidor tiene una GUI, no debe elegir esta identidad; Si lo hace, el usuario no podrá ver la interfaz de usuario.

Este tipo de servidor tiene un token principal y puede acceder a recursos remotos en los que un servidor que tenga la identidad launching-user podría no ser capaz de hacerlo. Para obtener más información sobre la suplantación y los tokens de acceso, vea [Niveles de suplantación](impersonation-levels.md) y [Arroba.](cloaking.md)

La ejecución como una cuenta de usuario fija es más segura que la identidad de usuario interactiva, ya que esta identidad solo la puede asignar alguien que tenga la contraseña del usuario específico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Identidad de aplicación](application-identity.md)
</dt> <dt>

[Usuario interactivo](interactive-user.md)
</dt> <dt>

[Iniciar usuario](launching-user.md)
</dt> <dt>

[Identidad de servicio](service-identity.md)
</dt> </dl>

 

 




