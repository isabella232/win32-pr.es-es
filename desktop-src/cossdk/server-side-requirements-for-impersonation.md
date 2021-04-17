---
description: Requisitos de Server-Side para la suplantación
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Requisitos de Server-Side para la suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714829"
---
# <a name="server-side-requirements-for-impersonation"></a>Requisitos de Server-Side para la suplantación

El servidor realiza la suplantación mediante programación. Asume explícitamente las credenciales de seguridad del cliente mediante [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Cuando el cliente ha concedido al servidor autoridad suficiente, tiene el efecto de sustituir las credenciales de seguridad del cliente por el token del subproceso del servidor, en lugar del token del proceso.

Una vez hecho esto, el servidor puede, por ejemplo, usar el token de cliente para tener acceso a los recursos protegidos con un descriptor de seguridad. O bien, puede realizar llamadas bajo la identidad del cliente, si está habilitada la ocultación.

El servidor puede establecer explícitamente la ocultación mediante programación o puede depender de una configuración administrativa. De forma predeterminada, las aplicaciones COM+ están configuradas para usar el Cloaking dinámico. Para obtener más información, consulte [Cloaking](cloaking.md).

Si el servidor está implementando la delegación en nombre del cliente, mediante la identidad del cliente a través de la red, la identidad del proceso del servidor debe marcarse como "de confianza para delegación" en el servicio Active Directory; de lo contrario, se producirá un error de delegación.

Cuando ha terminado de usar la identidad del cliente, el servidor puede revertir a su propio token de proceso mediante [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).

Para más información sobre cómo implementar la suplantación y la delegación, consulte [delegación y suplantación](/windows/desktop/com/delegation-and-impersonation).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos del cliente para la suplantación](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Esconder](cloaking.md)
</dt> </dl>

 

 
