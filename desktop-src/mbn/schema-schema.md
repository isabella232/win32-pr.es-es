---
description: Define un perfil de banda ancha móvil.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Referencia de esquema de Perfil de banda ancha móvil
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666504"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Referencia de esquema de Perfil de banda ancha móvil

El esquema de Perfil de banda ancha móvil define un perfil de banda ancha móvil.

Los perfiles almacenan los parámetros de configuración de red y de usuario relacionados con la conexión de banda ancha móvil. También almacenan las preferencias de usuario para una conexión.

El elemento raíz de un perfil de banda ancha móvil es el elemento [**MBNProfile**](schema-mbnprofile-element.md) . Cada perfil tiene exactamente un elemento raíz. Todos los elementos de esquema de Perfil de banda ancha móvil usados por Windows 7 se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v1` y los elementos usados por Windows 8 se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WWAN/profile/v2` .

El esquema de Perfil de banda ancha móvil exige estrictamente el orden de los nodos. Los nodos especificados en un perfil deben adherirse al **esquema de Perfil de banda ancha móvil** y aparecer en el orden indicado en la definición del esquema. Por ejemplo, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) debe especificarse inmediatamente después de [**AccessString**](schema-accessstring-contexttype-element.md).

-   [Esquema de Perfil de banda ancha móvil v1](mobile-broadband-profile-schema.md)
-   [Esquema de Perfil de banda ancha móvil V2](mobile-broadband-profile-schema-v2.md)
-   [Esquema de Perfil de banda ancha móvil V3](mobile-broadband-profile-schema-v3.md)
-   [Esquema de Perfil de banda ancha móvil V4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 
