---
description: Server-Side requisitos de suplantación
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side requisitos de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e43016428f2ff083fc5a783d05c3c79e241dcf299f3af9ca226cb4f6a2cf1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096805"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side requisitos de suplantación

El servidor realiza la suplantación mediante programación. Presupone explícitamente las credenciales de seguridad del cliente mediante [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Cuando el cliente ha concedido al servidor autoridad suficiente, esto tiene el efecto de sustituir las credenciales de seguridad del cliente por el token de subproceso de servidor, en lugar del token de proceso.

Una vez hecho esto, el servidor puede, por ejemplo, usar el token de cliente para acceder a los recursos que se protegen con un descriptor de seguridad. O bien, puede realizar llamadas en la identidad del cliente, si está habilitada la protección.

El servidor puede establecer explícitamente la creación mediante programación, o puede basarse en una configuración administrativa. De forma predeterminada, las aplicaciones COM+ están configuradas para usar el arroba dinámico. Para obtener más información, vea [La ingción de](cloaking.md).

Si el servidor implementa la delegación en nombre del cliente (mediante la identidad de cliente a través de la red), la identidad de proceso del servidor debe marcarse como "De confianza para la delegación" en el servicio Active Directory. De lo contrario, se producirá un error en la delegación.

Cuando haya terminado de usar la identidad del cliente, el servidor puede revertir a su propio token de proceso [**mediante CoRevertToSelf.**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

Para obtener más información sobre cómo implementar la suplantación y la delegación, vea [Delegación y suplantación.](/windows/desktop/com/delegation-and-impersonation)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisitos del lado cliente para la suplantación](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Ocultación](cloaking.md)
</dt> </dl>

 

 
