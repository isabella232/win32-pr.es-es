---
description: Esquema de perfil de banda ancha móvil v3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Esquema de perfil de banda ancha móvil v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168182"
---
# <a name="mobile-broadband-profile-schema-v3"></a>Esquema de perfil de banda ancha móvil v3

El Windows 8 Esquema de perfil de banda ancha móvil v3 está disponible en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v3` .

-   [Elementos del esquema de perfil de banda ancha móvil v3](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



