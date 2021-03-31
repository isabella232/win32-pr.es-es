---
description: Esquema de Perfil de banda ancha móvil V3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Esquema de Perfil de banda ancha móvil V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907920"
---
# <a name="mobile-broadband-profile-schema-v3"></a>Esquema de Perfil de banda ancha móvil V3

El esquema de Perfil de banda ancha de Windows 8Mobile V3 está disponible en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v3` .

-   [Elementos del esquema de Perfil de banda ancha móvil V3](mobile-broadband-profile-schema-v3-elements.md)

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

 

 



