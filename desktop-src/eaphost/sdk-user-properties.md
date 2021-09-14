---
title: Propiedades de usuario del SDK
description: Obtenga información sobre las propiedades de usuario del SDK. Vea un ejemplo que es una instancia del esquema nativo eaphostusercredentials.
ms.assetid: e8a9656d-48e7-4580-a84d-2b829e7a692f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c8dab154e1ef6c736849720856a23fdfe2e7b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358849"
---
# <a name="sdk-user-properties"></a>Propiedades de usuario del SDK

Este ejemplo es una instancia del esquema [nativo eaphostusercredentials.](eaphostusercredentialsschema-schema.md)

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

[Propiedades del usuario](user-profiles.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> </dl>

 

 




