---
description: Esquema de Perfil de banda ancha móvil V2.
ms.assetid: 0E140DCC-373C-44B3-8A91-F38AE7A5797C
title: Esquema de Perfil de banda ancha móvil V2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1328e2b108c80addc8f69584cd1b3cbd797ac777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154197"
---
# <a name="mobile-broadband-profile-schema-v2"></a><span data-ttu-id="dd839-103">Esquema de Perfil de banda ancha móvil V2</span><span class="sxs-lookup"><span data-stu-id="dd839-103">Mobile Broadband Profile Schema v2</span></span>

<span data-ttu-id="dd839-104">El esquema de Perfil de banda ancha de Windows 8Mobile V2 está disponible en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="dd839-104">The Windows 8Mobile Broadband Profile Schema v2 is available in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

-   [<span data-ttu-id="dd839-105">Elementos del esquema de Perfil de banda ancha móvil V2</span><span class="sxs-lookup"><span data-stu-id="dd839-105">Mobile Broadband Profile Schema v2 Elements</span></span>](mobile-broadband-profile-schema-v2-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v2"
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v2" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    xmlns:WWAN_profile_v1="https://www.microsoft.com/networking/WWAN/profile/v1" 
    elementFormDefault="qualified">

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v1" schemaLocation="WWAN_profile_v1.xsd"/>

    <!-- Flag to indicate whether this is a purchase profile, default is "false" -->
    <xs:element name="IsPurchaseProfile" type="xs:boolean"/>

    <!-- Display Provider Name -->
    <xs:element name="DisplayProviderName" type="WWAN_profile_v1:providerNameType"/>

</xs:schema>
```

 

 



