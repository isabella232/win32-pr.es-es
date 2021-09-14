---
title: Suplantación
description: La suplantación es la capacidad de un subproceso para ejecutarse en un contexto de seguridad diferente del contexto del proceso que posee el subproceso.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060930"
---
# <a name="impersonation"></a>Suplantación

La suplantación es la capacidad de un subproceso para ejecutarse en un contexto de seguridad diferente del contexto del proceso que posee el subproceso. Cuando se ejecuta en el contexto de seguridad del cliente, el servidor "es" el cliente, hasta cierto punto. El subproceso de servidor usa un token de acceso que representa las credenciales del cliente para obtener acceso a los objetos a los que tiene acceso el cliente.

El motivo principal de la suplantación es hacer que se realicen comprobaciones de acceso con la identidad del cliente. Si se usa la identidad del cliente para las comprobaciones de acceso, el acceso se puede restringir o expandir, en función de los permisos que tenga el cliente. Por ejemplo, supongamos que un servidor de archivos tiene archivos que contienen información confidencial y que cada uno de estos archivos está protegido por una ACL. Para ayudar a evitar que un cliente obtenga acceso no autorizado a la información de estos archivos, el servidor puede suplantar al cliente antes de acceder a los archivos.

## <a name="access-tokens-for-impersonation"></a>Tokens de acceso para la suplantación

Los tokens de acceso son objetos que describen el contexto de seguridad de un proceso o subproceso. Proporcionan información que incluye la identidad de una cuenta de usuario y un subconjunto de los privilegios disponibles para la cuenta de usuario. Cada proceso tiene un *token de acceso principal* que describe el contexto de seguridad de la cuenta de usuario asociada al proceso. De forma predeterminada, el sistema usa el token principal cuando un subproceso del proceso interactúa con un objeto protegible. Sin embargo, cuando un subproceso suplanta a un cliente, el subproceso de suplantación tiene un token de acceso principal y un *token de suplantación.* El token de suplantación representa el contexto de seguridad del cliente y este token de acceso es el que se usa para las comprobaciones de acceso durante la suplantación. Cuando la suplantación ha terminado, el subproceso vuelve a usar solo el token de acceso principal.

Puede usar la [**función OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para obtener un identificador para el token principal de un proceso. Use la [**función OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener un identificador para el token de suplantación de un subproceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tokens de acceso](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> </dl>

 

 