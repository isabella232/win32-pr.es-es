---
title: Propiedades de usuario de MS-CHAPv2 PEAP
description: Obtenga información sobre las propiedades de usuario de MS-CHAPv2 PEAP. Vea un ejemplo que es una instancia del esquema heredado mschapv2userpropertiesv1.
ms.assetid: af1ed6b1-712e-4b55-9ab4-b6b38f486fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b2d3d48e35c300be2baf9c563c8168f5914a39
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421524"
---
# <a name="peap-ms-chapv2-user-properties"></a><span data-ttu-id="bf601-104">Propiedades de usuario de MS-CHAPv2 PEAP</span><span class="sxs-lookup"><span data-stu-id="bf601-104">PEAP MS-CHAPv2 User Properties</span></span>

<span data-ttu-id="bf601-105">Este ejemplo es una instancia del esquema heredado [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="bf601-105">This sample is an instance of the [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) legacy schema.</span></span>

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
      xmlns:MsChapV2="https://www.microsoft.com/provisioning/MsChapV2UserPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <MsPeap:EapType>
          <MsPeap:RoutingIdentity>test</MsPeap:RoutingIdentity> 
          <baseEap:Eap>
            <baseEap:Type>26</baseEap:Type> 
            <MsChapV2:EapType>
              <MsChapV2:Username>test</MsChapV2:Username> 
              <MsChapV2:Password>test</MsChapV2:Password> 
              <MsChapV2:LogonDomain>ias-domain</MsChapV2:LogonDomain> 
            </MsChapV2:EapType>
          </baseEap:Eap>
        </MsPeap:EapType>
      </baseEap:Eap>
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="bf601-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf601-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf601-107">Propiedades de usuario</span><span class="sxs-lookup"><span data-stu-id="bf601-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="bf601-108">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="bf601-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




