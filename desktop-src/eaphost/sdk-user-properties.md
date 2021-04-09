---
title: Propiedades de usuario de SDK
description: Obtenga información sobre las propiedades de usuario del SDK. Vea un ejemplo que es una instancia del esquema nativo eaphostusercredentials.
ms.assetid: e8a9656d-48e7-4580-a84d-2b829e7a692f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c8dab154e1ef6c736849720856a23fdfe2e7b3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149697"
---
# <a name="sdk-user-properties"></a>Propiedades de usuario de SDK

Este ejemplo es una instancia del esquema nativo [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .

``` syntax
  <?xml version="1.0" ?>  
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod> 
    <Credentials>
      <EapType>40</EapType> 
      <Identity>test</Identity> 
      <Password>test</Password> 
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de usuario](user-profiles.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> </dl>

 

 




