---
title: Propiedades de usuario PEAP-TLS
description: Obtenga información sobre las propiedades de usuario PEAP-TLS. Vea un ejemplo que es una instancia del esquema heredado eaptlsuserpropertiesv1.
ms.assetid: f0fb00fa-4cf8-4490-ac59-a8252ddcb5ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32437c54d707c3d278e4494c2b5b4f56ed83c9d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240788"
---
# <a name="peap-tls-user-properties"></a>Propiedades de usuario PEAP-TLS

Este ejemplo es una instancia del esquema [heredado eaptlsuserpropertiesv1.](eaptlsuserpropertiesv1schema-schema.md)

``` syntax
  <?xml version="1.0" ?> 
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon"
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1"
      xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1"
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsUserPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <MsPeap:EapType>
          <MsPeap:RoutingIdentity>test</MsPeap:RoutingIdentity> 
          <baseEap:Eap>
            <baseEap:Type>13</baseEap:Type> 
            <eapTls:EapType>
              <eapTls:Username>ias-domain\test</eapTls:Username> 
              <eapTls:UserCert /> 
            </eapTls:EapType>
          </baseEap:Eap>
        </MsPeap:EapType>
      </baseEap:Eap>
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del usuario](user-profiles.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> </dl>

 

 




