---
title: Escritorio remoto interfaces de puerta de enlace
description: La API Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) admite las interfaces siguientes. Puede usar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374694"
---
# <a name="remote-desktop-gateway-interfaces"></a>Escritorio remoto interfaces de puerta de enlace

La API Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) admite las interfaces siguientes. Puede usar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas. No hay ninguna dependencia entre el complemento de autenticación y el complemento de autorización, y solo puede implementar un único complemento si lo desea.

Los complementos de autenticación son [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) [**y ITSGAuthenticationEngine.**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)

Los complementos de autorización son [**ITSGAccountingEngine,**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine) [**ITSGAuthorizeConnectionSink,**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink) [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)y [**ITSGPolicyEngine.**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Expone métodos que proporcionan información sobre la creación o el cierre de sesiones para una conexión.

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Expone métodos que notifican a Puerta de enlace de Escritorio remoto sobre eventos de autenticación.

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Expone métodos que autentican a los usuarios para la puerta de enlace de Escritorio remoto.

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Expone métodos que notifican a puerta de enlace de Escritorio remoto el resultado de un intento de autorizar una conexión.

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Expone métodos que notifican a puerta de enlace de Escritorio remoto el resultado de un intento de autorización de un recurso.

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Expone métodos que autorizan conexiones y recursos.

</dd> </dl>

 

 




