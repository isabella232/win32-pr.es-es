---
title: MSAA no está disponible para las aplicaciones de la tienda Windows
description: MSAA no está disponible para las aplicaciones de la tienda Windows
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078505"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA no está disponible para las aplicaciones de la tienda Windows

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


## <a name="description"></a>Descripción

Windows 8 no es compatible con MSAA (Microsoft Active Accessibility) para leer o automatizar datos accesibles desde aplicaciones de la tienda Windows. En su lugar, se debe usar la API de automatización de la interfaz de usuario (UIA), disponible desde Windows 7. Dado que no hay ninguna característica existente de la aplicación de la tienda Windows, no hay implementaciones existentes que se vean afectadas por este cambio. Esto afecta solo a las nuevas aplicaciones y características escritas para Windows 8. Los desarrolladores pueden seguir usando MSAA para exponer sus datos de accesibilidad. Si el proveedor de aplicaciones de la tienda Windows proporciona los datos de MSAA, los clientes de UIA todavía podrán leer y automatizar los datos.

Para simplificar la API de las aplicaciones de la tienda Windows 8Windows, decidimos admitir solo la automatización de la interfaz de usuario como cliente para estas aplicaciones. Los clientes de UIA pueden leer proveedores de UIA de forma nativa, sin traducción. Los clientes de UIA pueden leer proveedores de MSAA como traducidos a través del proxy de UIA a MSAA. Esto reducirá la carga de pruebas de los desarrolladores de aplicaciones de la tienda Windows.

La eliminación de la compatibilidad con los proveedores de MSAA reduciría aún más la matriz de pruebas, pero hay aplicaciones importantes que siguen estando basadas en MSAA y no queremos representarlas inaccesibles.

## <a name="manifestation"></a>Manifestación

Los desarrolladores de aplicaciones de la tienda Windows no podrán acceder a los detalles de MSAA en el modelo de aplicación.

## <a name="solution"></a>Solución

No se deben crear nuevos casos automatizados en MSAA para las características de las aplicaciones de la tienda Windows.

Cambie las herramientas integradas existentes que usan MSAA a UIA si necesitan interactuar con las aplicaciones de la tienda Windows. Los desarrolladores de aplicaciones de la tienda Windows deben usar la API de automatización de la interfaz de usuario.

## <a name="resources"></a>Recursos

-   [Fundamentos de UI Automation](../winauto/entry-uiauto-win32.md)

 

 