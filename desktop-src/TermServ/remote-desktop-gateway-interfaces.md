---
title: Interfaces de puerta de enlace de Escritorio remoto
description: La API de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) admite las siguientes interfaces. Puede utilizar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993957"
---
# <a name="remote-desktop-gateway-interfaces"></a>Interfaces de puerta de enlace de Escritorio remoto

La API de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) admite las siguientes interfaces. Puede utilizar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas. No hay ninguna dependencia entre el complemento de autenticación y el complemento de autorización, y solo puede implementar un complemento si lo desea.

Los complementos de autenticación son [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) y [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

Los complementos de autorización son [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)y [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Expone métodos que proporcionan información sobre la creación o el cierre de sesiones para una conexión.

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Expone métodos que notifican a la puerta de enlace de escritorio remoto sobre eventos de autenticación.

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Expone métodos que autentican a los usuarios para la puerta de enlace de escritorio remoto.

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Expone métodos que envían una notificación a la puerta de enlace de escritorio remoto sobre el resultado de un intento de autorizar una conexión.

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Expone métodos que envían una notificación a la puerta de enlace de escritorio remoto sobre el resultado de un intento de autorizar un recurso.

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Expone métodos que autorizan conexiones y recursos.

</dd> </dl>

 

 




