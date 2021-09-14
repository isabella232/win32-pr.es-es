---
title: Propiedades de conexión PEAP-TLS
description: Obtenga información sobre las propiedades de conexión PEAP-TLS. Vea un ejemplo que es una instancia del esquema heredado eaptlsconnectionpropertiesv1.
ms.assetid: 1128b3f7-eba7-484e-a3d8-070d37e9c57f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa368ca49b93cff8fa3cd60620ec075bfb8d3a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240789"
---
# <a name="peap-tls-connection-properties"></a>Propiedades de conexión PEAP-TLS

Este ejemplo es una instancia del esquema [heredado eaptlsconnectionpropertiesv1.](eaptlsconnectionpropertiesv1schema-schema.md)

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon"
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1"
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1"
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <msPeap:EapType>
          <msPeap:ServerValidation>
            <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
            <msPeap:ServerNames /> 
            <msPeap:TrustedRootCA /> 
          </msPeap:ServerValidation>
          <msPeap:FastReconnect>true</msPeap:FastReconnect> 
          <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
          <baseEap:Eap>
            <baseEap:Type>13</baseEap:Type> 
            <eapTls:EapType>
              <eapTls:CredentialsSource>
                <eapTls:CertificateStore /> 
              </eapTls:CredentialsSource>
              <eapTls:ServerValidation>
                <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                <eapTls:ServerNames /> 
                <eapTls:TrustedRootCA /> 
              </eapTls:ServerValidation>
              <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
            </eapTls:EapType>
          </baseEap:Eap>
          <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
          <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
        </msPeap:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de conexión](connection-profiles.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> </dl>

 

 




