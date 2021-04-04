---
title: Propiedades de conexión EAP-TLS
description: Obtenga información acerca de las propiedades de conexión EAP-TLS. Vea un ejemplo que es una instancia del esquema heredado eaptlsconnectionpropertiesv1.
ms.assetid: 7d8e7771-5263-4187-bb9d-ec0d6c154b17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbda4f345c0feedf6571f9f1c58f0193a876d2d1
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797116"
---
# <a name="eap-tls-connection-properties"></a>Propiedades de conexión EAP-TLS

Este ejemplo es una instancia del esquema heredado [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) .

``` syntax
  <?xml version="1.0" ?>
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>13</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
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
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de conexión](connection-profiles.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> </dl>

 

 




