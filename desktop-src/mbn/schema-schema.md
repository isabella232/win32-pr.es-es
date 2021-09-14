---
description: Define un perfil de banda ancha móvil.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Referencia de esquema de perfil de banda ancha móvil
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252531"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Referencia de esquema de perfil de banda ancha móvil

El esquema de perfil de banda ancha móvil define un perfil de banda ancha móvil.

Los perfiles almacenan parámetros de configuración de red y usuario relacionados con la conexión de banda ancha móvil. También almacenan las preferencias del usuario para una conexión.

El elemento raíz de un perfil de banda ancha móvil es el [**elemento MBNProfile.**](schema-mbnprofile-element.md) Cada perfil tiene exactamente un elemento raíz. Todos los elementos del esquema de perfil de banda ancha móvil usados por Windows 7 se encuentran en el espacio de nombres y los elementos utilizados por Windows 8 están `https://www.microsoft.com/networking/WWAN/profile/v1` en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v2` .

El esquema de perfil de banda ancha móvil aplica estrictamente el orden de los nodos. Los nodos especificados en un perfil deben cumplir el **esquema** de perfil de banda ancha móvil y aparecer en el orden indicado en la definición del esquema. Por ejemplo, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) debe especificarse inmediatamente después de [**AccessString.**](schema-accessstring-contexttype-element.md)

-   [Esquema de perfil de banda ancha móvil v1](mobile-broadband-profile-schema.md)
-   [Esquema de perfil de banda ancha móvil v2](mobile-broadband-profile-schema-v2.md)
-   [Esquema de perfil de banda ancha móvil v3](mobile-broadband-profile-schema-v3.md)
-   [Esquema de perfil de banda ancha móvil v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 
