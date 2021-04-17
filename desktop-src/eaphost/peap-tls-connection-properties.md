---
title: Propiedades de conexión PEAP-TLS
description: Obtenga información sobre las propiedades de conexión PEAP-TLS. Vea un ejemplo que es una instancia del esquema heredado eaptlsconnectionpropertiesv1.
ms.assetid: 1128b3f7-eba7-484e-a3d8-070d37e9c57f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa368ca49b93cff8fa3cd60620ec075bfb8d3a5
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104533556"
---
# <a name="peap-tls-connection-properties"></a><span data-ttu-id="aae08-104">Propiedades de conexión PEAP-TLS</span><span class="sxs-lookup"><span data-stu-id="aae08-104">PEAP-TLS Connection Properties</span></span>

<span data-ttu-id="aae08-105">Este ejemplo es una instancia del esquema heredado [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="aae08-105">This sample is an instance of the [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) legacy schema..</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="aae08-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aae08-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae08-107">Propiedades de conexión</span><span class="sxs-lookup"><span data-stu-id="aae08-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="aae08-108">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="aae08-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




